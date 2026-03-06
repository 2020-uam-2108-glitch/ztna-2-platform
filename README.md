# 🔐 ZTNA 2.0 — Zero Trust Network Access Platform

A fully interactive **Zero Trust Network Access (ZTNA) 2.0** security platform dashboard built with React. This project demonstrates the architecture, features, and UI of an enterprise-grade ZTNA solution.

![ZTNA 2.0 Platform](https://img.shields.io/badge/Security-ZTNA%202.0-00d4ff?style=for-the-badge&logo=shield)
![React](https://img.shields.io/badge/React-18.2-61DAFB?style=for-the-badge&logo=react)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 🚀 Features

### 🔐 Simulated ZTNA Login Flow
- Multi-step authentication: Credentials → MFA → Device Posture Scan
- Simulates biometric, FIDO2, passkey, and TOTP auth methods
- Real-time device posture verification checklist

### 🖥️ SOC Dashboard
- Live auto-refreshing session counters and threat metrics
- Real-time security alerts with severity levels (Critical / High / Medium / Low)
- Per-user risk scoring and risk bar visualization
- Threat intelligence feed (IOC / TTP / CVE indicators)

### 🪪 Identity & Authentication Module
- Full user identity registry with behavioral risk breakdown
- MFA method strength comparison (FIDO2 → SMS)
- Clickable user profiles with force-MFA and terminate-session controls
- Risk factor drill-down (behavioral anomaly, geo-velocity, device posture, threat intel)

### 💻 Device Trust Engine
- Device inventory with compliance scores, encryption, AV, MDM status
- Trust Level classification (Level 0–4)
- Fleet-wide posture check pass/fail rates (8 checks)

### ⚙️ Policy Engine
- YAML-rendered policy rules (name, conditions, actions)
- Live access simulation: shows ALLOW/DENY per user based on policy
- Policy creation UI placeholder

### 🔀 Micro-Segmentation Map
- Visual network map: Users → ZTNA Broker → Applications
- Just-In-Time (JIT) access request tracking
- Active encrypted tunnel monitoring
- Blocked attempt log

### 📊 Analytics & UEBA
- 24-hour authentication event bar chart
- User Behavior Analytics with per-user deviation scoring
- Compliance scorecards: NIST CSF, ISO 27001, SOC 2, GDPR, PCI-DSS, HIPAA

---

## 🛠️ Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Framework   | React 18 + Hooks                  |
| Styling     | Inline CSS (no build deps needed) |
| Fonts       | Share Tech Mono, Rajdhani (Google Fonts) |
| State       | useState / useEffect              |
| Build       | Create React App                  |

---

## 📦 Getting Started

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/ztna-2-platform.git
cd ztna-2-platform

# Install dependencies
npm install

# Start development server
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
```

---

## 📁 Project Structure

```
ztna-2-platform/
├── public/
│   └── index.html
├── src/
│   ├── constants/
│   │   ├── theme.js          # Color palette & helper functions
│   │   └── data.js           # Mock users, devices, policies, alerts
│   ├── components/
│   │   ├── UI.jsx            # Shared UI primitives (Badge, Panel, RiskBar...)
│   │   ├── LoginScreen.jsx   # 3-step ZTNA authentication flow
│   │   ├── DashboardTab.jsx  # SOC Dashboard
│   │   ├── IdentityTab.jsx   # Identity & Auth module
│   │   ├── DeviceTab.jsx     # Device Trust module
│   │   ├── PolicyTab.jsx     # Policy Engine module
│   │   ├── SegmentTab.jsx    # Micro-Segmentation module
│   │   └── AnalyticsTab.jsx  # Analytics & UEBA module
│   ├── App.jsx               # Main app shell & navigation
│   └── index.js              # React entry point
├── package.json
└── README.md
```

---

## 🏗️ Architecture Overview

```
┌──────────────────────────────────────────────────────┐
│                  ZTNA 2.0 CONTROL PLANE              │
│   Identity Engine  │  Policy Engine  │  AI Risk Engine│
└──────────────────────────────────────────────────────┘
              │              │              │
┌──────────────────────────────────────────────────────┐
│               DATA PLANE (Enforcement)               │
│   Connectors   │   Proxies   │  Micro-Segmentation   │
└──────────────────────────────────────────────────────┘
              │              │              │
┌──────────────────────────────────────────────────────┐
│          ENDPOINTS / USERS / DEVICES / APPS          │
└──────────────────────────────────────────────────────┘
```

---

## 🔒 ZTNA 2.0 Principles Demonstrated

- **Never Trust, Always Verify** — Every user, device, and session is continuously evaluated
- **Least Privilege Access** — Policy engine grants minimum required access
- **Assume Breach** — Real-time anomaly detection, session recording, DLP controls
- **Continuous Monitoring** — Risk scores recalculated in real-time during sessions
- **AI-Driven Decisions** — Behavioral biometrics and UEBA for adaptive policies

---

## 📊 Compliance Frameworks Covered

| Framework     | Coverage                             |
|---------------|--------------------------------------|
| NIST CSF 2.0  | Identify, Protect, Detect, Respond   |
| ISO 27001     | Access control, Cryptography         |
| SOC 2 Type II | CC6 (Logical Access), CC7 (Sys Ops)  |
| GDPR / NIS2   | Data minimization, breach detection  |
| PCI-DSS v4.0  | Network segmentation, MFA, audit     |
| HIPAA         | PHI access controls, audit trails    |

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

> Built as a demonstration of ZTNA 2.0 architecture and UI/UX concepts. All data is simulated.
