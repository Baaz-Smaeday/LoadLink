<p align="center">
  <img src="assets/images/loadlink-banner.png" alt="LoadLink" width="600">
</p>

<h1 align="center">LoadLink</h1>

<p align="center">
  <strong>The UK's first platform connecting businesses directly to courier drivers.</strong><br>
  No middlemen. No phone calls. Book, track, deliver, get paid — all in one place.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.2.0-blue?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/phase-2%20of%204-green?style=flat-square" alt="Phase">
  <img src="https://img.shields.io/badge/license-MIT-orange?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/status-in%20development-yellow?style=flat-square" alt="Status">
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square" alt="PRs Welcome">
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-demo">Demo</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-roadmap">Roadmap</a> •
  <a href="#-contributing">Contributing</a> •
  <a href="#-license">License</a>
</p>

---

## 🚀 What is LoadLink?

LoadLink is a transport marketplace that connects **businesses** who need deliveries with **courier drivers** who can deliver them — instantly.

Think of it as **Uber for courier deliveries**, but built specifically for the UK transport industry.

### The Problem

Currently, businesses needing urgent deliveries must:
1. Call a courier company
2. Who then posts the job on an exchange (like Courier Exchange)
3. Where drivers compete on price
4. Adding multiple middlemen and delays

**Courier Exchange** (the current market leader) charges drivers **£2,300+/year** with 12-month lock-in contracts, offers only one booking method (quotes), and runs on outdated technology.

### Our Solution

LoadLink cuts out the middlemen and offers:

| Feature | Courier Exchange | LoadLink |
|---------|:---:|:---:|
| Booking modes | 1 (quotes only) | **3** (quotes + fixed price + driver availability) |
| Instant booking | ❌ | ✅ Uber-style |
| Driver availability posts | ❌ | ✅ |
| Customer tracking links | ❌ | ✅ Shareable |
| Digital POD (photo + signature) | Basic | ✅ Full (photo + sig + GPS + timestamp) |
| Auto invoicing | ❌ | ✅ |
| Direct business booking | ❌ | ✅ |
| Mobile apps | 3 separate apps | **1 unified app** |
| Driver pricing | £2,300+/year locked | **£49-79/month or free + 8%** |
| Contract | 12-month lock-in | **Cancel anytime** |

---

## ✨ Features

### 3 Booking Modes

- **💬 Quote Request** — Post a load, drivers send their prices, pick the best one
- **⚡ Fixed Price (Uber-style)** — Set your price, nearest driver accepts instantly
- **📍 Driver Availability** — Drivers post their location, vehicle & rate. Businesses book them directly

### 4 User Types

- 🏭 **Direct Businesses** — Book transport with zero industry knowledge needed
- 📦 **Freight Forwarders** — Manage loads, preferred carriers, customer tracking
- 🏢 **Courier Companies** — Fleet management, dispatch, subbie networks
- 🚐 **Owner Drivers** — Find loads, post availability, get paid fast

### Phase 2 Features (Current)

- 📍 **Live GPS Tracking** — Real-time map with animated van, ETA, status updates
- 📸 **Digital POD** — Photo evidence + signature pad + GPS stamp + timestamp
- ⭐ **Rating & Reviews** — 5-star system with written reviews and driver profiles
- 💰 **Payments** — Wallet, transaction history, instant payout option
- 📄 **Auto Invoicing** — Generated on POD submission, payment reminders at 7/14/30 days
- 🔔 **Push Notifications** — New loads, quote accepted, reviews, payments, POD confirmations

---

## 🎮 Demo

### Quick Start

1. Download `src/LoadLink-Phase2.html`
2. Double-click to open in any browser
3. That's it — no install, no setup

### Screenshots

<p align="center">
  <img src="assets/images/screenshot-home.png" alt="Home" width="250">
  <img src="assets/images/screenshot-booking.png" alt="Booking" width="250">
  <img src="assets/images/screenshot-tracking.png" alt="Tracking" width="250">
</p>

> Screenshots coming soon — take them from the live prototype!

---

## 🏗 Getting Started

### Prerequisites

For the **prototype** (Phase 1-2): Nothing! Just a web browser.

For the **production build** (Phase 3+):
- Node.js 18+
- npm or yarn
- PostgreSQL 15+
- Redis
- Stripe account

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/loadlink.git

# Open the prototype
cd loadlink
open src/LoadLink-Phase2.html
```

### Project Structure

```
loadlink/
├── src/                          # Source code
│   ├── LoadLink-Phase1-MVP.html  # Phase 1 prototype
│   ├── LoadLink-Phase2.html      # Phase 2 prototype (current)
│   └── components/               # Reusable components (coming Phase 3)
├── docs/                         # Documentation
│   ├── ARCHITECTURE.md           # System architecture
│   ├── API.md                    # API documentation
│   ├── FEATURES.md               # Detailed feature specs
│   └── BUSINESS-PLAN.md          # Business model & pricing
├── assets/                       # Static assets
│   ├── images/                   # Screenshots, banners
│   └── icons/                    # App icons, favicons
├── .github/                      # GitHub config
│   └── ISSUE_TEMPLATE/           # Issue templates
├── README.md                     # This file
├── ROADMAP.md                    # Development roadmap
├── CHANGELOG.md                  # Version history
├── CONTRIBUTING.md               # How to contribute
├── LICENSE                       # MIT License
├── CODE_OF_CONDUCT.md            # Community guidelines
├── package.json                  # Project metadata
└── .gitignore                    # Git ignore rules
```

---

## 🗺 Roadmap

| Phase | Status | Features |
|-------|--------|----------|
| **Phase 1 — MVP** | ✅ Complete | User registration, load posting, 3 booking modes, driver availability, dashboards |
| **Phase 2 — Core** | ✅ Complete | GPS tracking, digital POD, ratings, payments, invoicing, notifications |
| **Phase 3 — Growth** | 🔄 Next | Native mobile apps, analytics, compliance, route optimisation, fleet tools, API |
| **Phase 4 — Scale** | 📋 Planned | AI matching, automated pricing, multi-language, European expansion |

See [ROADMAP.md](ROADMAP.md) for detailed breakdown.

---

## 💰 Business Model

- **Businesses**: 8-12% per transaction (no subscription needed)
- **Drivers**: Free tier + 8% commission OR £49-79/month Pro
- **Freight Forwarders**: £79-149/month subscription
- **Courier Companies**: £29-49/vehicle/month
- **Instant Payout**: 2-3% fee per payout
- **Featured Listings**: £10-30/week

---

## 🛠 Tech Stack

| Layer | Technology | Why |
|-------|-----------|-----|
| Frontend | React / Next.js | Fast, modern, mobile-responsive |
| Mobile | React Native | One codebase → iOS + Android |
| Backend | Node.js | Real-time, scalable |
| Database | PostgreSQL + Redis | Reliable + fast caching |
| Maps | Google Maps / Mapbox | Live tracking, routing |
| Payments | Stripe Connect | Marketplace payments, instant payouts |
| Real-time | WebSockets / Socket.io | Live tracking, notifications |
| Hosting | AWS / Vercel | Auto-scaling, reliable |

---

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

---

## 📞 Contact

- **Email**: hello@loadlink.co.uk
- **Twitter**: [@LoadLinkUK](https://twitter.com/LoadLinkUK)
- **Website**: [loadlink.co.uk](https://loadlink.co.uk) *(coming soon)*

---

<p align="center">
  <strong>Built with ❤️ for the UK courier industry</strong><br>
  <sub>Fed up with overpriced exchanges? So were we.</sub>
</p>
