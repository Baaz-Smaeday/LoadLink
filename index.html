import { useState, useEffect, useRef } from "react";

const FEATURES = [
  { icon: "⚡", title: "Instant Booking", desc: "Tap accept, job booked. No calls, no emails, no waiting.", tag: "CX can't do this" },
  { icon: "🤖", title: "AI Load Matching", desc: "Smart algorithms match you to loads based on location, vehicle, history & route.", tag: "Industry first" },
  { icon: "📍", title: "Live GPS Tracking", desc: "Real-time map with ETA, status updates, and shareable customer tracking links.", tag: "Better than CX" },
  { icon: "📸", title: "Digital POD", desc: "Photo + e-signature + GPS stamp + timestamp. Bulletproof proof of delivery.", tag: "Better than CX" },
  { icon: "💰", title: "Instant Payouts", desc: "Get paid same day. No 30-day waits. Stripe-powered instant to your bank.", tag: "CX can't do this" },
  { icon: "🛣️", title: "Route Optimisation", desc: "AI backload matching. Never drive home empty. Save hundreds in dead miles.", tag: "CX can't do this" },
  { icon: "🏆", title: "Carrier Tiers", desc: "Gold, Silver, Bronze. Better performance = lower commission + priority loads.", tag: "Industry first" },
  { icon: "📊", title: "Analytics Dashboard", desc: "Earnings, rates/mile, dead miles, fuel costs, demand heatmaps — all live.", tag: "Better than CX" },
  { icon: "⚖️", title: "Dispute Resolution", desc: "AI-assisted fair dispute handling. Evidence-based, resolved within 48hrs.", tag: "CX can't do this" },
];

const COMPARE = [
  { feat: "Booking modes", cx: "1", ll: "3", win: true },
  { feat: "Instant booking", cx: "✗", ll: "✓", win: true },
  { feat: "Driver availability posts", cx: "✗", ll: "✓", win: true },
  { feat: "AI load matching", cx: "✗", ll: "✓", win: true },
  { feat: "Smart pricing engine", cx: "✗", ll: "✓", win: true },
  { feat: "Customer tracking portal", cx: "✗", ll: "✓", win: true },
  { feat: "Digital POD", cx: "Basic", ll: "Full", win: true },
  { feat: "Instant payouts", cx: "✗", ll: "✓", win: true },
  { feat: "Route optimisation", cx: "✗", ll: "✓", win: true },
  { feat: "Fleet management", cx: "Basic", ll: "Full", win: true },
  { feat: "Loyalty rewards", cx: "✗", ll: "✓", win: true },
  { feat: "Carrier tiers", cx: "✗", ll: "✓", win: true },
  { feat: "Monthly price", cx: "£190+", ll: "FREE", win: true },
  { feat: "Contract", cx: "12 months", ll: "None", win: true },
];

const TESTIMONIALS = [
  { name: "James M.", role: "Owner Driver, Leeds", text: "I was paying CX £2,300 a year for one booking mode. LoadLink gives me three modes, AI matching, and it's free to start. No brainer.", rating: 5, avatar: "JM" },
  { name: "Sarah K.", role: "Fleet Manager, Manchester", text: "Managing 4 drivers across 3 apps was a nightmare. Now everything's in one dashboard — tracking, POD, payments, compliance. Game changer.", rating: 5, avatar: "SK" },
  { name: "AutoFix Ltd", role: "Shipping Client, Birmingham", text: "We used to wait hours for a driver. Now we post a fixed price, someone accepts in 30 seconds. Our customers get a tracking link too.", rating: 5, avatar: "AF" },
];

const STATS = [
  { n: "60s", l: "Average booking time" },
  { n: "80%", l: "Cheaper than CX" },
  { n: "3", l: "Booking modes" },
  { n: "0", l: "Lock-in contracts" },
];

const MODES = [
  { num: "01", icon: "💬", title: "Quote Request", desc: "Post a job, drivers compete. Pick the best price. Like CX — but with better tools, tracking and instant POD.", color: "#3b82f6", tag: "Familiar" },
  { num: "02", icon: "⚡", title: "Fixed Price", desc: "Set your price. Nearest driver taps Accept. Booked in seconds. No haggling, no waiting. Uber for freight.", color: "#f59e0b", tag: "Game changer" },
  { num: "03", icon: "📍", title: "Driver Availability", desc: "Drivers post: 'I'm in London, heading to Leeds, LWB Sprinter, £1.10/mi.' Businesses book them directly.", color: "#8b5cf6", tag: "Industry first" },
];

function useInView(threshold = 0.15) {
  const ref = useRef(null);
  const [visible, setVisible] = useState(false);
  useEffect(() => {
    const el = ref.current;
    if (!el) return;
    const obs = new IntersectionObserver(([e]) => { if (e.isIntersecting) setVisible(true); }, { threshold });
    obs.observe(el);
    return () => obs.disconnect();
  }, [threshold]);
  return [ref, visible];
}

function AnimatedSection({ children, delay = 0, className = "" }) {
  const [ref, visible] = useInView();
  return (
    <div ref={ref} className={className} style={{ opacity: visible ? 1 : 0, transform: visible ? "translateY(0)" : "translateY(40px)", transition: `all 0.7s cubic-bezier(0.16, 1, 0.3, 1) ${delay}s` }}>
      {children}
    </div>
  );
}

function CountUp({ target, suffix = "", prefix = "" }) {
  const [count, setCount] = useState(0);
  const [ref, visible] = useInView();
  useEffect(() => {
    if (!visible) return;
    const num = parseInt(target) || 0;
    if (num === 0) { setCount(0); return; }
    let start = 0;
    const step = Math.max(1, Math.floor(num / 40));
    const timer = setInterval(() => {
      start += step;
      if (start >= num) { setCount(num); clearInterval(timer); }
      else setCount(start);
    }, 30);
    return () => clearInterval(timer);
  }, [visible, target]);
  return <span ref={ref}>{prefix}{count}{suffix}</span>;
}

export default function LoadLinkLanding() {
  const [hoveredFeat, setHoveredFeat] = useState(null);
  const [mobileMenu, setMobileMenu] = useState(false);

  return (
    <div style={{ background: "#050a14", color: "#e2e8f0", fontFamily: "'Syne', 'DM Sans', system-ui, sans-serif", overflowX: "hidden" }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=Outfit:wght@300;400;500;600;700&display=swap');
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { background: #050a14; }
        .glow-amber { text-shadow: 0 0 40px rgba(245,158,11,0.3) }
        .glass { background: rgba(255,255,255,0.03); backdrop-filter: blur(20px); border: 1px solid rgba(255,255,255,0.06) }
        .glass-strong { background: rgba(255,255,255,0.05); backdrop-filter: blur(30px); border: 1px solid rgba(255,255,255,0.08) }
        @keyframes float { 0%,100% { transform: translateY(0px) } 50% { transform: translateY(-10px) } }
        @keyframes shimmer { 0% { background-position: -200% center } 100% { background-position: 200% center } }
        @keyframes pulse-ring { 0% { transform: scale(1); opacity: 0.6 } 100% { transform: scale(2.5); opacity: 0 } }
        @keyframes gradient-shift { 0% { background-position: 0% 50% } 50% { background-position: 100% 50% } 100% { background-position: 0% 50% } }
        .shimmer-text { background: linear-gradient(90deg, #f59e0b, #fbbf24, #f59e0b, #fbbf24); background-size: 200%; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: shimmer 3s linear infinite }
        .gradient-border { position: relative }
        .gradient-border::before { content: ''; position: absolute; inset: -1px; border-radius: inherit; padding: 1px; background: linear-gradient(135deg, rgba(245,158,11,0.4), rgba(139,92,246,0.4), rgba(59,130,246,0.4)); -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0); -webkit-mask-composite: xor; mask-composite: exclude; pointer-events: none }
        .nav-blur { background: rgba(5,10,20,0.8); backdrop-filter: blur(20px); border-bottom: 1px solid rgba(255,255,255,0.05) }
        .hover-lift { transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1) }
        .hover-lift:hover { transform: translateY(-4px) }
        .btn-glow { position: relative; overflow: hidden }
        .btn-glow::after { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 60%); opacity: 0; transition: opacity 0.3s }
        .btn-glow:hover::after { opacity: 1 }
        .section-pad { padding: 120px 24px }
        .max-w { max-width: 1140px; margin: 0 auto }
        .feat-card { transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1) }
        .feat-card:hover { transform: translateY(-6px) scale(1.02); border-color: rgba(245,158,11,0.3) !important }
        .compare-row { transition: all 0.2s }
        .compare-row:hover { background: rgba(255,255,255,0.03) }
        .noise-overlay { position: fixed; inset: 0; opacity: 0.015; pointer-events: none; z-index: 0; background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E") }
      `}</style>

      <div className="noise-overlay" />

      {/* NAV */}
      <nav className="nav-blur" style={{ position: "fixed", top: 0, width: "100%", zIndex: 100, padding: "14px 24px" }}>
        <div className="max-w" style={{ display: "flex", alignItems: "center", justifyContent: "space-between" }}>
          <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
            <div style={{ background: "linear-gradient(135deg, #f59e0b, #ea580c)", borderRadius: 10, width: 36, height: 36, display: "flex", alignItems: "center", justifyContent: "center", fontWeight: 900, color: "#fff", fontSize: 13, fontFamily: "Outfit" }}>LL</div>
            <span style={{ fontSize: 20, fontWeight: 800, color: "#fff", letterSpacing: -0.5 }}>LoadLink</span>
          </div>
          <div style={{ display: "flex", alignItems: "center", gap: 32 }}>
            {["Features", "Compare", "Pricing", "Demo"].map(l => (
              <a key={l} href={`#${l.toLowerCase()}`} style={{ fontSize: 13, color: "#94a3b8", fontWeight: 500, textDecoration: "none", fontFamily: "Outfit", transition: "0.2s" }}
                onMouseEnter={e => e.target.style.color = "#fff"} onMouseLeave={e => e.target.style.color = "#94a3b8"}>{l}</a>
            ))}
            <a href="https://github.com/Baaz-Smaeday/LoadLink" target="_blank" rel="noreferrer"
              style={{ fontSize: 13, color: "#94a3b8", fontWeight: 500, textDecoration: "none", fontFamily: "Outfit" }}>GitHub</a>
            <button className="btn-glow" style={{ background: "linear-gradient(135deg, #f59e0b, #ea580c)", color: "#fff", padding: "9px 22px", borderRadius: 50, fontSize: 13, fontWeight: 700, border: "none", cursor: "pointer", fontFamily: "Outfit" }}>
              Launch App →
            </button>
          </div>
        </div>
      </nav>

      {/* HERO */}
      <section style={{ minHeight: "100vh", display: "flex", flexDirection: "column", alignItems: "center", justifyContent: "center", textAlign: "center", padding: "140px 24px 100px", position: "relative" }}>
        {/* Gradient orbs */}
        <div style={{ position: "absolute", top: "10%", left: "20%", width: 500, height: 500, background: "radial-gradient(circle, rgba(245,158,11,0.07) 0%, transparent 70%)", pointerEvents: "none" }} />
        <div style={{ position: "absolute", bottom: "10%", right: "15%", width: 400, height: 400, background: "radial-gradient(circle, rgba(59,130,246,0.05) 0%, transparent 70%)", pointerEvents: "none" }} />
        <div style={{ position: "absolute", top: "50%", left: "50%", transform: "translate(-50%,-50%)", width: 600, height: 600, background: "radial-gradient(circle, rgba(139,92,246,0.04) 0%, transparent 70%)", pointerEvents: "none" }} />

        <AnimatedSection>
          <div style={{ display: "inline-flex", alignItems: "center", gap: 8, background: "rgba(245,158,11,0.08)", border: "1px solid rgba(245,158,11,0.15)", borderRadius: 50, padding: "6px 18px", marginBottom: 32 }}>
            <div style={{ width: 7, height: 7, background: "#fbbf24", borderRadius: "50%", animation: "float 3s ease-in-out infinite" }} />
            <span style={{ color: "#fbbf24", fontSize: 12, fontWeight: 600, letterSpacing: 1, fontFamily: "Outfit" }}>NOW IN DEVELOPMENT</span>
          </div>
        </AnimatedSection>

        <AnimatedSection delay={0.1}>
          <h1 style={{ fontSize: "clamp(40px, 7vw, 80px)", fontWeight: 800, lineHeight: 1.05, letterSpacing: -3, marginBottom: 24, maxWidth: 800 }}>
            <span style={{ color: "#fff" }}>Transport booked</span><br />
            <span className="shimmer-text">in under 60 seconds.</span>
          </h1>
        </AnimatedSection>

        <AnimatedSection delay={0.2}>
          <p style={{ fontSize: "clamp(16px, 2vw, 20px)", color: "#64748b", maxWidth: 520, lineHeight: 1.8, marginBottom: 44, fontFamily: "Outfit", fontWeight: 400 }}>
            The UK's first platform connecting businesses directly to courier drivers. No middlemen. No phone calls. AI-powered matching.
          </p>
        </AnimatedSection>

        <AnimatedSection delay={0.3}>
          <div style={{ display: "flex", gap: 14, flexWrap: "wrap", justifyContent: "center", marginBottom: 72 }}>
            <button className="btn-glow hover-lift" style={{ background: "linear-gradient(135deg, #f59e0b, #ea580c)", color: "#fff", padding: "16px 36px", borderRadius: 16, fontSize: 16, fontWeight: 700, border: "none", cursor: "pointer", fontFamily: "Outfit", boxShadow: "0 8px 32px rgba(245,158,11,0.25)" }}>
              🚀 Try Live Prototype
            </button>
            <button className="hover-lift" style={{ background: "rgba(255,255,255,0.04)", color: "#fff", padding: "16px 36px", borderRadius: 16, fontSize: 16, fontWeight: 700, border: "1px solid rgba(255,255,255,0.08)", cursor: "pointer", fontFamily: "Outfit" }}>
              View on GitHub
            </button>
          </div>
        </AnimatedSection>

        <AnimatedSection delay={0.4}>
          <div style={{ display: "flex", gap: 48, justifyContent: "center", flexWrap: "wrap" }}>
            {STATS.map((s, i) => (
              <div key={i} style={{ textAlign: "center" }}>
                <div style={{ fontSize: 36, fontWeight: 800, color: "#fff", fontFamily: "Syne" }}>
                  {s.n === "0" ? "£0" : s.n}
                </div>
                <div style={{ fontSize: 13, color: "#475569", fontFamily: "Outfit", marginTop: 4 }}>{s.l}</div>
              </div>
            ))}
          </div>
        </AnimatedSection>
      </section>

      {/* SOCIAL PROOF BAR */}
      <div style={{ borderTop: "1px solid rgba(255,255,255,0.05)", borderBottom: "1px solid rgba(255,255,255,0.05)", padding: "20px 24px", background: "rgba(255,255,255,0.01)" }}>
        <div className="max-w" style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 40, flexWrap: "wrap" }}>
          {["🇬🇧 Built in the UK", "🛡️ MIT Open Source", "⚡ 3 Booking Modes", "🤖 AI-Powered", "💰 Free to Start", "📱 Mobile Ready"].map((t, i) => (
            <span key={i} style={{ fontSize: 13, color: "#475569", fontFamily: "Outfit", fontWeight: 500, whiteSpace: "nowrap" }}>{t}</span>
          ))}
        </div>
      </div>

      {/* 3 MODES */}
      <section id="features" className="section-pad">
        <div className="max-w">
          <AnimatedSection>
            <div style={{ textAlign: "center", marginBottom: 64 }}>
              <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 16, fontFamily: "Outfit" }}>HOW IT WORKS</div>
              <h2 style={{ fontSize: "clamp(32px, 4vw, 52px)", fontWeight: 800, color: "#fff", letterSpacing: -2, marginBottom: 16 }}>3 ways to move goods.</h2>
              <p style={{ fontSize: 17, color: "#64748b", maxWidth: 480, margin: "0 auto", fontFamily: "Outfit", lineHeight: 1.7 }}>Courier Exchange gives you one. We give you three.</p>
            </div>
          </AnimatedSection>

          <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 20 }}>
            {MODES.map((m, i) => (
              <AnimatedSection key={i} delay={i * 0.1}>
                <div className="glass hover-lift gradient-border" style={{ borderRadius: 24, padding: 36, height: "100%", position: "relative", overflow: "hidden" }}>
                  <div style={{ position: "absolute", top: 20, right: 24, fontSize: 64, fontWeight: 900, color: "rgba(255,255,255,0.02)", fontFamily: "Syne" }}>{m.num}</div>
                  <div style={{ width: 56, height: 56, borderRadius: 16, background: `${m.color}15`, display: "flex", alignItems: "center", justifyContent: "center", fontSize: 28, marginBottom: 20 }}>{m.icon}</div>
                  <div style={{ display: "inline-block", padding: "4px 12px", borderRadius: 20, fontSize: 11, fontWeight: 700, background: `${m.color}15`, color: m.color, marginBottom: 14, fontFamily: "Outfit" }}>{m.tag}</div>
                  <h3 style={{ fontSize: 22, fontWeight: 700, color: "#fff", marginBottom: 10, fontFamily: "Syne" }}>{m.title}</h3>
                  <p style={{ fontSize: 14, color: "#94a3b8", lineHeight: 1.7, fontFamily: "Outfit" }}>{m.desc}</p>
                </div>
              </AnimatedSection>
            ))}
          </div>
        </div>
      </section>

      {/* FEATURES GRID */}
      <section style={{ padding: "80px 24px 120px" }}>
        <div className="max-w">
          <AnimatedSection>
            <div style={{ textAlign: "center", marginBottom: 64 }}>
              <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 16, fontFamily: "Outfit" }}>FEATURES</div>
              <h2 style={{ fontSize: "clamp(32px, 4vw, 52px)", fontWeight: 800, color: "#fff", letterSpacing: -2, marginBottom: 16 }}>Everything. One platform.</h2>
            </div>
          </AnimatedSection>

          <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 16 }}>
            {FEATURES.map((f, i) => (
              <AnimatedSection key={i} delay={i * 0.05}>
                <div
                  className="feat-card"
                  onMouseEnter={() => setHoveredFeat(i)}
                  onMouseLeave={() => setHoveredFeat(null)}
                  style={{
                    background: hoveredFeat === i ? "rgba(255,255,255,0.05)" : "rgba(255,255,255,0.02)",
                    border: "1px solid rgba(255,255,255,0.06)",
                    borderRadius: 20, padding: 28, cursor: "default", height: "100%"
                  }}
                >
                  <div style={{ fontSize: 28, marginBottom: 14 }}>{f.icon}</div>
                  <h3 style={{ fontSize: 16, fontWeight: 700, color: "#fff", marginBottom: 6, fontFamily: "Syne" }}>{f.title}</h3>
                  <p style={{ fontSize: 13, color: "#64748b", lineHeight: 1.6, fontFamily: "Outfit", marginBottom: 12 }}>{f.desc}</p>
                  <span style={{ fontSize: 11, fontWeight: 600, color: f.tag.includes("first") ? "#a78bfa" : f.tag.includes("can't") ? "#f59e0b" : "#60a5fa", fontFamily: "Outfit" }}>{f.tag}</span>
                </div>
              </AnimatedSection>
            ))}
          </div>
        </div>
      </section>

      {/* COMPARISON TABLE */}
      <section id="compare" style={{ padding: "100px 24px", background: "rgba(255,255,255,0.01)", borderTop: "1px solid rgba(255,255,255,0.04)", borderBottom: "1px solid rgba(255,255,255,0.04)" }}>
        <div className="max-w" style={{ maxWidth: 800 }}>
          <AnimatedSection>
            <div style={{ textAlign: "center", marginBottom: 56 }}>
              <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 16, fontFamily: "Outfit" }}>COMPARISON</div>
              <h2 style={{ fontSize: "clamp(32px, 4vw, 52px)", fontWeight: 800, color: "#fff", letterSpacing: -2, marginBottom: 16 }}>LoadLink vs Courier Exchange</h2>
              <p style={{ fontSize: 17, color: "#64748b", fontFamily: "Outfit" }}>Feature by feature. There's no contest.</p>
            </div>
          </AnimatedSection>

          <AnimatedSection delay={0.1}>
            <div className="glass" style={{ borderRadius: 24, overflow: "hidden" }}>
              <div style={{ display: "grid", gridTemplateColumns: "1fr 100px 100px", padding: "16px 24px", borderBottom: "1px solid rgba(255,255,255,0.06)", background: "rgba(255,255,255,0.02)" }}>
                <span style={{ fontSize: 12, fontWeight: 700, color: "#475569", fontFamily: "Outfit", textTransform: "uppercase", letterSpacing: 1 }}>Feature</span>
                <span style={{ fontSize: 12, fontWeight: 700, color: "#475569", fontFamily: "Outfit", textAlign: "center", textTransform: "uppercase", letterSpacing: 1 }}>CX</span>
                <span style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", fontFamily: "Outfit", textAlign: "center", textTransform: "uppercase", letterSpacing: 1 }}>LoadLink</span>
              </div>
              {COMPARE.map((c, i) => (
                <div key={i} className="compare-row" style={{ display: "grid", gridTemplateColumns: "1fr 100px 100px", padding: "14px 24px", borderBottom: i < COMPARE.length - 1 ? "1px solid rgba(255,255,255,0.03)" : "none" }}>
                  <span style={{ fontSize: 14, color: "#e2e8f0", fontFamily: "Outfit", fontWeight: i >= 12 ? 700 : 400 }}>{c.feat}</span>
                  <span style={{ fontSize: 14, color: c.cx === "✗" ? "#ef4444" : "#64748b", textAlign: "center", fontFamily: "Outfit" }}>{c.cx}</span>
                  <span style={{ fontSize: 14, color: "#22c55e", textAlign: "center", fontWeight: 700, fontFamily: "Outfit" }}>{c.ll}</span>
                </div>
              ))}
            </div>
          </AnimatedSection>
        </div>
      </section>

      {/* PRICING */}
      <section id="pricing" className="section-pad">
        <div className="max-w" style={{ maxWidth: 800 }}>
          <AnimatedSection>
            <div style={{ textAlign: "center", marginBottom: 56 }}>
              <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 16, fontFamily: "Outfit" }}>PRICING</div>
              <h2 style={{ fontSize: "clamp(32px, 4vw, 52px)", fontWeight: 800, color: "#fff", letterSpacing: -2, marginBottom: 16 }}>Fair pricing. Zero lock-in.</h2>
            </div>
          </AnimatedSection>

          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 20 }}>
            <AnimatedSection delay={0.1}>
              <div style={{ background: "rgba(239,68,68,0.04)", border: "1px solid rgba(239,68,68,0.12)", borderRadius: 24, padding: 36 }}>
                <div style={{ fontSize: 12, fontWeight: 700, color: "#ef4444", letterSpacing: 1, fontFamily: "Outfit", marginBottom: 12 }}>❌ COURIER EXCHANGE</div>
                <div style={{ fontSize: 44, fontWeight: 800, color: "#fca5a5", fontFamily: "Syne" }}>£190+</div>
                <div style={{ fontSize: 14, color: "#64748b", fontFamily: "Outfit", marginBottom: 24 }}>per month · 12-month lock-in</div>
                {["12-month contract", "No cancellation", "Price tripled since 2015", "No free tier", "Only 1 booking mode"].map((f, i) => (
                  <div key={i} style={{ display: "flex", alignItems: "center", gap: 8, padding: "6px 0", fontSize: 14, color: "#94a3b8", fontFamily: "Outfit" }}>
                    <span style={{ color: "#ef4444" }}>✗</span> {f}
                  </div>
                ))}
              </div>
            </AnimatedSection>

            <AnimatedSection delay={0.2}>
              <div className="gradient-border" style={{ background: "rgba(34,197,94,0.04)", borderRadius: 24, padding: 36, position: "relative" }}>
                <div style={{ position: "absolute", top: -1, left: "50%", transform: "translateX(-50%)", background: "linear-gradient(135deg, #f59e0b, #22c55e)", padding: "4px 16px", borderRadius: "0 0 12px 12px", fontSize: 11, fontWeight: 700, color: "#fff", fontFamily: "Outfit" }}>RECOMMENDED</div>
                <div style={{ fontSize: 12, fontWeight: 700, color: "#22c55e", letterSpacing: 1, fontFamily: "Outfit", marginBottom: 12, marginTop: 8 }}>✓ LOADLINK</div>
                <div style={{ fontSize: 44, fontWeight: 800, color: "#86efac", fontFamily: "Syne" }}>FREE</div>
                <div style={{ fontSize: 14, color: "#64748b", fontFamily: "Outfit", marginBottom: 24 }}>8% commission · or Pro from £49/mo</div>
                {["Free tier — pay when you earn", "Pro: £49-79/month flat fee", "Cancel anytime, no lock-in", "80% cheaper than CX", "3 booking modes + AI matching"].map((f, i) => (
                  <div key={i} style={{ display: "flex", alignItems: "center", gap: 8, padding: "6px 0", fontSize: 14, color: "#94a3b8", fontFamily: "Outfit" }}>
                    <span style={{ color: "#22c55e" }}>✓</span> {f}
                  </div>
                ))}
              </div>
            </AnimatedSection>
          </div>
        </div>
      </section>

      {/* TESTIMONIALS */}
      <section style={{ padding: "80px 24px 120px" }}>
        <div className="max-w">
          <AnimatedSection>
            <div style={{ textAlign: "center", marginBottom: 56 }}>
              <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 16, fontFamily: "Outfit" }}>TESTIMONIALS</div>
              <h2 style={{ fontSize: "clamp(28px, 4vw, 44px)", fontWeight: 800, color: "#fff", letterSpacing: -2 }}>What our beta testers say.</h2>
            </div>
          </AnimatedSection>

          <div style={{ display: "grid", gridTemplateColumns: "repeat(3, 1fr)", gap: 20 }}>
            {TESTIMONIALS.map((t, i) => (
              <AnimatedSection key={i} delay={i * 0.1}>
                <div className="glass hover-lift" style={{ borderRadius: 24, padding: 32 }}>
                  <div style={{ display: "flex", gap: 2, marginBottom: 16 }}>
                    {[...Array(t.rating)].map((_, j) => <span key={j} style={{ color: "#f59e0b", fontSize: 16 }}>★</span>)}
                  </div>
                  <p style={{ fontSize: 15, color: "#cbd5e1", lineHeight: 1.7, fontFamily: "Outfit", fontStyle: "italic", marginBottom: 20 }}>"{t.text}"</p>
                  <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
                    <div style={{ width: 40, height: 40, borderRadius: "50%", background: "linear-gradient(135deg, #f59e0b, #ea580c)", display: "flex", alignItems: "center", justifyContent: "center", fontWeight: 700, fontSize: 13, color: "#fff", fontFamily: "Outfit" }}>{t.avatar}</div>
                    <div>
                      <div style={{ fontSize: 14, fontWeight: 700, color: "#fff", fontFamily: "Outfit" }}>{t.name}</div>
                      <div style={{ fontSize: 12, color: "#475569", fontFamily: "Outfit" }}>{t.role}</div>
                    </div>
                  </div>
                </div>
              </AnimatedSection>
            ))}
          </div>
        </div>
      </section>

      {/* CTA */}
      <section id="demo" style={{ padding: "120px 24px", textAlign: "center", position: "relative" }}>
        <div style={{ position: "absolute", top: "50%", left: "50%", transform: "translate(-50%,-50%)", width: 700, height: 500, background: "radial-gradient(circle, rgba(245,158,11,0.06) 0%, transparent 70%)", pointerEvents: "none" }} />
        <AnimatedSection>
          <div style={{ fontSize: 12, fontWeight: 700, color: "#f59e0b", letterSpacing: 2, textTransform: "uppercase", marginBottom: 20, fontFamily: "Outfit" }}>READY?</div>
          <h2 style={{ fontSize: "clamp(36px, 5vw, 60px)", fontWeight: 800, color: "#fff", letterSpacing: -2, marginBottom: 20 }}>See it in action.</h2>
          <p style={{ fontSize: 18, color: "#64748b", maxWidth: 500, margin: "0 auto 44px", fontFamily: "Outfit", lineHeight: 1.7 }}>
            Full interactive prototype. Try both sides — business and driver. See what CX should have been.
          </p>
          <div style={{ display: "flex", gap: 14, justifyContent: "center", flexWrap: "wrap" }}>
            <button className="btn-glow hover-lift" style={{ background: "linear-gradient(135deg, #f59e0b, #ea580c)", color: "#fff", padding: "18px 44px", borderRadius: 16, fontSize: 18, fontWeight: 700, border: "none", cursor: "pointer", fontFamily: "Outfit", boxShadow: "0 12px 40px rgba(245,158,11,0.3)" }}>
              🚀 Launch Prototype
            </button>
          </div>
          <p style={{ color: "#334155", fontSize: 13, marginTop: 24, fontFamily: "Outfit" }}>Open source · MIT License · Built in Leeds, UK 🇬🇧</p>
        </AnimatedSection>
      </section>

      {/* FOOTER */}
      <footer style={{ borderTop: "1px solid rgba(255,255,255,0.04)", padding: "40px 24px", textAlign: "center" }}>
        <div style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 10, marginBottom: 12 }}>
          <div style={{ background: "linear-gradient(135deg, #f59e0b, #ea580c)", borderRadius: 8, width: 28, height: 28, display: "flex", alignItems: "center", justifyContent: "center", fontWeight: 900, color: "#fff", fontSize: 10 }}>LL</div>
          <span style={{ fontSize: 16, fontWeight: 800, color: "#fff" }}>LoadLink</span>
        </div>
        <p style={{ fontSize: 13, color: "#334155", fontFamily: "Outfit" }}>The Courier Exchange alternative — better features, fairer pricing, built for drivers.</p>
        <p style={{ fontSize: 12, color: "#1e293b", fontFamily: "Outfit", marginTop: 8 }}>© 2026 LoadLink · <a href="https://github.com/Baaz-Smaeday/LoadLink" style={{ color: "#f59e0b", textDecoration: "none" }}>GitHub</a></p>
      </footer>
    </div>
  );
}
