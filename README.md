# 💚 MoneyBridge

> **Universal Financial Freedom for Everyone**
> Built for students, the needy & entrepreneurs across the world.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Author](https://img.shields.io/badge/Author-molich023-brightgreen)](https://github.com/molich023)
[![M-Pesa](https://img.shields.io/badge/Payment-M--Pesa%20Daraja%202.0-00A550)](https://developer.safaricom.co.ke)
[![Security](https://img.shields.io/badge/Security-OWASP%20Top%2010-blue)](https://owasp.org)
[![GDPR](https://img.shields.io/badge/Compliant-GDPR%20%7C%20HIPAA-orange)](https://gdpr.eu)
[![Countries](https://img.shields.io/badge/Countries-40%2B-yellow)](https://github.com/molich023/moneybridge)

---

## 👤 Original Developer

| Field | Detail |
|-------|--------|
| **GitHub** | [@molich023](https://github.com/molich023) |
| **Project** | MoneyBridge |
| **Started** | 2024 |
| **License** | MIT (Open Source) |
| **M-Pesa** | 0704658022 |
| **IP Anchor** | Blockchain (Phase 2) |

> ⚠️ This project was **conceived, designed and authored by molich023**.
> Open source contributions are welcome but original authorship is retained.

---

## 🌍 What Is MoneyBridge?

MoneyBridge is a **universal financial access app** that works in any country,
on any Android phone, with or without a bank account.

- 🆓 **1 month free trial** — no card required
- 💳 **KSH 100/year** (~$0.77) after trial — the world's most affordable financial app
- 📲 **M-Pesa payments** via Safaricom Daraja 2.0 STK Push
- 🌐 **150+ currencies** supported with real-time conversion
- 🔐 **Bank-level security** — OWASP Top 10 compliant
- 📡 **Offline mode** — works in low-connectivity areas
- 🎓 **Student toolkit** — budgeting, savings, scholarship alerts
- 🤝 **Referral earnings** — KSH 20 per referral

---

## 🗂 Repository Structure

```
moneybridge/
│
├── frontend/
│   └── index.html          # Complete website (single file)
│
├── backend/
│   ├── server.js           # Node.js + Express + M-Pesa Daraja
│   ├── package.json        # Dependencies
│   └── .env.example        # Environment variables template
│
├── blockchain/
│   └── anchor.js           # Phase 2: Hash codebase to blockchain
│
├── docs/
│   └── LAUNCH_GUIDE.md     # Step-by-step deployment guide
│
├── scripts/
│   └── setup-repo.sh       # Auto-setup script
│
├── .github/
│   └── workflows/
│       └── deploy.yml      # CI/CD pipeline
│
├── LICENSE                 # MIT + IP Notice
└── README.md               # This file
```

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- M-Pesa Daraja API credentials ([developer.safaricom.co.ke](https://developer.safaricom.co.ke))

### Local Development
```bash
# Clone the repo
git clone https://github.com/molich023/moneybridge.git
cd moneybridge

# Install dependencies
cd backend && npm install

# Configure environment
cp .env.example .env
nano .env  # Add your M-Pesa credentials

# Start server
node server.js

# Open in browser
# http://localhost:3000
```

### Android (Termux) Setup
```bash
pkg update && pkg upgrade
pkg install nodejs git
git clone https://github.com/molich023/moneybridge.git
cd moneybridge/backend
npm install
node server.js
# Visit http://localhost:3000 in Chrome
```

---

## 💳 Payment Integration

MoneyBridge uses the **official Safaricom Daraja 2.0 API** for M-Pesa payments.

```
M-Pesa Business Number: 0704658022
Payment Flow:           STK Push → Customer PIN → Instant Confirmation
Sandbox Testing:        Use phone 254708374149 with any PIN
```

### Currency Equivalents of KSH 100
| Country | Currency | Amount |
|---------|----------|--------|
| Kenya | KES | KSH 100 |
| USA | USD | $0.77 |
| Europe | EUR | €0.71 |
| UK | GBP | £0.61 |
| Nigeria | NGN | ₦1,170 |
| South Africa | ZAR | R14.20 |
| Ghana | GHS | ₵11.50 |
| India | INR | ₹64 |

---

## 🔐 Security Architecture

| Layer | Implementation |
|-------|---------------|
| **OWASP A01** | Route-level authorization checks |
| **OWASP A02** | TLS 1.3, no plaintext secrets |
| **OWASP A03** | Parameterized SQL, input sanitization |
| **OWASP A05** | Helmet.js, strict CSP + HSTS |
| **OWASP A07** | Rate limiting: 5 payment attempts/hour |
| **OWASP A09** | Morgan logging, zero PII in logs |
| **GDPR** | Consent recording, right to erasure endpoint |
| **HIPAA** | No health data stored, access controls |

---

## ⛓ Blockchain Phase (Phase 2)

After initial deployment, the codebase will be **anchored to blockchain**:

```
1. SHA-256 hash of entire codebase generated
2. Hash submitted to Ethereum/Polygon network
3. Transaction hash stored in /blockchain/proof.json
4. Immutable, decentralized proof of authorship created
5. No central authority can alter or dispute this record
```

This creates **triple-layered IP protection:**
- ✅ GitHub commit timestamps (centralized)
- ✅ MIT License with author attribution (legal)
- ✅ Blockchain hash anchor (immutable/decentralized)

---

## 🗺 Roadmap

- [x] **Phase 1** — Core website + M-Pesa integration
- [x] **Phase 1** — OWASP/GDPR/HIPAA compliance
- [x] **Phase 1** — GitHub repository + MIT License
- [ ] **Phase 2** — Blockchain IP anchoring
- [ ] **Phase 2** — Flutterwave (non-M-Pesa countries)
- [ ] **Phase 2** — Android APK (wrap with Capacitor.js)
- [ ] **Phase 3** — Dashboard & referral tracking UI
- [ ] **Phase 3** — Multi-language support (Swahili, French, Hindi)
- [ ] **Phase 4** — DeFi integration for savings yield

---

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repo
2. Create a branch: `git checkout -b feature/your-feature`
3. Commit with clear messages
4. Open a Pull Request

**Note:** Original authorship (molich023) remains in all forks per MIT License terms.

---

## 📜 License

MIT License — see [LICENSE](LICENSE) for full details.

**Original Author:** molich023
**Copyright:** © 2024 molich023. All rights reserved under MIT terms.
**Brand:** "MoneyBridge" is a trademark of molich023.

---

<div align="center">
  <strong>Built with ❤️ for the world's underserved</strong><br/>
  <em>By molich023 — making financial freedom universal, one KSH 100 at a time.</em>
</div>
