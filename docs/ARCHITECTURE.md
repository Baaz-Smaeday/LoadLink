# 🏗 System Architecture

## Overview

LoadLink is a multi-sided marketplace connecting 4 user types through a real-time transport booking platform.

## Architecture Diagram

```
┌─────────────────────────────────────────────────────────┐
│                      CLIENTS                             │
│                                                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│  │ Web App  │  │ iOS App  │  │ Android  │              │
│  │ (React)  │  │ (React   │  │ (React   │              │
│  │          │  │  Native) │  │  Native) │              │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘              │
│       │              │              │                    │
└───────┼──────────────┼──────────────┼────────────────────┘
        │              │              │
        ▼              ▼              ▼
┌─────────────────────────────────────────────────────────┐
│                    API GATEWAY                           │
│              (Authentication, Rate Limiting)             │
└────────────────────────┬────────────────────────────────┘
                         │
        ┌────────────────┼────────────────┐
        ▼                ▼                ▼
┌──────────────┐ ┌──────────────┐ ┌──────────────┐
│  Booking     │ │  Tracking    │ │  Payments    │
│  Service     │ │  Service     │ │  Service     │
│              │ │              │ │              │
│ • Load CRUD  │ │ • GPS ingest │ │ • Stripe     │
│ • Matching   │ │ • ETA calc   │ │ • Invoicing  │
│ • Quoting    │ │ • Geofencing │ │ • Payouts    │
│ • Dispatch   │ │ • History    │ │ • Ledger     │
└──────┬───────┘ └──────┬───────┘ └──────┬───────┘
       │                │                │
       ▼                ▼                ▼
┌─────────────────────────────────────────────────────────┐
│                     DATA LAYER                           │
│                                                          │
│  ┌──────────────┐  ┌────────────┐  ┌────────────────┐  │
│  │ PostgreSQL   │  │   Redis    │  │  S3 / Storage  │  │
│  │              │  │            │  │                │  │
│  │ • Users      │  │ • Sessions │  │ • POD photos   │  │
│  │ • Loads      │  │ • Cache    │  │ • Documents    │  │
│  │ • Bookings   │  │ • Pub/Sub  │  │ • Signatures   │  │
│  │ • Invoices   │  │ • Queues   │  │ • Invoices PDF │  │
│  │ • Reviews    │  │            │  │                │  │
│  └──────────────┘  └────────────┘  └────────────────┘  │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

## Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React / Next.js | Web application |
| **Mobile** | React Native | iOS + Android apps |
| **API** | Node.js + Express | REST API + WebSocket |
| **Database** | PostgreSQL | Primary data store |
| **Cache** | Redis | Sessions, real-time data, pub/sub |
| **Storage** | AWS S3 | Photos, documents, signatures |
| **Maps** | Google Maps / Mapbox | Tracking, routing, geocoding |
| **Payments** | Stripe Connect | Marketplace payments |
| **Real-time** | Socket.io | Live tracking, notifications |
| **Email** | SendGrid | Transactional emails |
| **SMS** | Twilio | SMS notifications |
| **Hosting** | AWS / Vercel | Auto-scaling infrastructure |
| **CI/CD** | GitHub Actions | Automated testing & deployment |

## Data Models

### Core Entities

```
User
├── id, email, phone, password_hash
├── role (business | driver | forwarder | courier_company)
├── company_name, rating, jobs_completed
├── vehicle_type, location, availability_status
└── stripe_account_id

Load
├── id, shipper_id, driver_id
├── booking_mode (quote | fixed_price | availability)
├── pickup_address, delivery_address
├── vehicle_required, weight, description
├── urgency, special_requirements[]
├── status (posted | quoted | booked | collecting | transit | delivered | cancelled)
├── price, service_tier
└── created_at, updated_at

Quote
├── id, load_id, driver_id
├── price, message
├── status (pending | accepted | rejected | expired)
└── created_at

Tracking
├── id, load_id, driver_id
├── latitude, longitude, speed, heading
├── eta_minutes
├── share_token (for customer links)
└── timestamp

POD (Proof of Delivery)
├── id, load_id
├── photo_url, signature_url
├── gps_lat, gps_lng
├── recipient_name
├── delivered_at
└── verified (boolean)

Invoice
├── id, load_id, from_user_id, to_user_id
├── amount, platform_fee, net_amount
├── status (draft | sent | paid | overdue)
├── due_date, paid_at
└── pdf_url

Review
├── id, load_id, from_user_id, to_user_id
├── rating (1-5), text
└── created_at

Notification
├── id, user_id
├── type, title, message
├── read (boolean)
└── created_at
```

## Real-time Architecture

```
Driver GPS Update → WebSocket → Server → Redis Pub/Sub
                                              │
                    ┌─────────────────────────┤
                    ▼                         ▼
              Update DB               Push to subscribers
              (every 30s)            (shipper, customer link)
```

## Security

- JWT authentication with refresh tokens
- Rate limiting on all endpoints
- Input validation & sanitisation
- HTTPS everywhere
- Stripe PCI compliance for payments
- GDPR compliant data handling
- Document encryption at rest

## Scaling Strategy

1. **Phase 1-2**: Single server, managed DB
2. **Phase 3**: Horizontal scaling, CDN, read replicas
3. **Phase 4**: Microservices, container orchestration, multi-region
