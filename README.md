# Hi there, I'm Patrick Sean Odugboche 👋

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&pause=1000&color=60A5FA&center=true&vCenter=true&width=650&lines=AI-Native+Full-Stack+%26+Systems+Engineer;High-Throughput+Backends+in+Go+%26+Python;Real-Time+WebRTC%2C+Sockets+%26+Mobile+Architect;Algorithmic+Trading+%26+Risk+Engine+Builder;Building+Autonomous+AI-Driven+Platforms" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/patrick-sean-odugboche-826115176"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/Jaytricks35"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="Twitter / X" /></a>
  <a href="https://www.instagram.com/jaytricks_oche"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" /></a>
  <a href="mailto:odu.pisc@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://komarev.com/ghpvc/?username=Podugboch&color=00ADD8&style=for-the-badge&label=Profile+Views" alt="Profile Views" />
</p>

---

## 🚀 About Me

I am an **AI-Native Full-Stack & Systems Engineer** driven by building fault-tolerant backend services, high-throughput real-time protocols, algorithmic trading infrastructure, and mobile-native user experiences.

- ⚙️ **Systems & Concurrency**: Designing concurrent, asynchronous architectures in **Go (Golang)** and **Python** (WebSockets, WebRTC mesh, Redis clustering, multi-exchange execution engines).
- 🌐 **Modern Frontend & Mobile**: Crafting fast, responsive client applications with **React 19**, **TypeScript**, **Tailwind CSS**, and **Capacitor** for native Android and cross-platform distribution.
- 🤖 **AI-Native Integration**: Integrating conversational AI models (Google Gemini) grounded in real-time geospatial telemetry, microclimate forecasting, and domain-specific heuristics.
- 🛡️ **Security & Robustness**: Practicing zero-trust secret handling, hardware kill switches, strict risk-gate filters, and comprehensive data validation.
- ⚡ **Engineering Philosophy**: *"Design for extreme conditions, test against reality without lookahead bias, and build software that stays resilient when scale spikes."*

---

## 📌 Pinned Repositories

Detailed engineering breakdown of flagship systems:

| Project Name        | Category           | Tech Stack                  |
| :------------------ | :----------------- | :-------------------------- |
| 1. BOT              | Algorithmic Engine | ccxt, Python, Risk Layer    |
| 2. Nesty            | Real-Time Social   | Go, WebRTC, React 19, Redis |
| 3. Auram            | AI Travel & Office | Gemini AI, React, Capacitor |
| 4. Cluster-4-Roster | Facility Rotation  | TanStack Start, TypeScript  |

---

### 1. 🪙 [BOT — Trader Queen: Algorithmic Multi-Exchange Trading System](https://github.com/Podugboch/BOT)

[![Repository](https://img.shields.io/badge/GitHub-Podugboch%2FBOT-181717?style=flat-square&logo=github)](https://github.com/Podugboch/BOT)
[![Language](https://img.shields.io/badge/Language-Python%203.11+-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/Podugboch/BOT)
[![Framework](https://img.shields.io/badge/Exchange%20Engine-CCXT%20100+-F7931A?style=flat-square)](https://github.com/ccxt/ccxt)
[![Architecture](https://img.shields.io/badge/Risk%20Layer-Circuit%20Breaker%20%2B%20KillSwitch-red?style=flat-square)](#)
[![Testing](https://img.shields.io/badge/Test%20Suite-PyTest%20Passed-4493F8?style=flat-square&logo=pytest&logoColor=white)](#)

> **An institutional-grade algorithmic cryptocurrency trading engine and quantitative backtester built on `ccxt`, supporting 100+ spot and derivatives exchanges with multi-stage mathematical entry filters, strict capital protection rules, and an asynchronous management dashboard.**

#### 📐 Core Architecture & Signal Pipeline
1. **Stage 1 (Core Trend & Momentum Trigger)**: Dual Exponential Moving Average (fast/slow EMA) crossover validated against Relative Strength Index (RSI) momentum and Average Directional Index (ADX) trend-strength thresholds to eliminate sideways and choppy market noise.
2. **Stage 2 (Dynamic Fibonacci Retracement Filter)**: Rolling anchor lookback window (default 50 bars) computing automatic 38.2%, 50%, and 61.8% pullback zones with Average True Range (ATR) scaled dynamic tolerance bands (`fib_tolerance_atr_mult`). Includes signal touch persistence (`fib_touch_window`) to prevent signal starvation.
3. **Stage 3 (Strict Capital & Risk Gate)**: Volatility-adjusted position sizing, fee-and-slippage simulation identical across backtest, paper trading, and live execution.

#### 🛡️ Built-in Risk Management & Circuit Breakers
- **Multi-Level Circuit Breakers**: Automatic trading suspension upon hitting daily maximum loss limits or consecutive losing streaks.
- **Dynamic Trailing Stops & Hard Cutoffs**: Strict stop-loss calculation before any order enters the exchange pipeline.
- **Instant Kill Switch**: Emergency hardware kill trigger via filesystem file drop (`touch KILL`), causing the engine to cleanly disengage on the next loop cycle.
- **Asynchronous Live Web Dashboard**: Self-hosted, lightweight management console (`web_server.py`) with SQLite session auth (`auth.py`), user management (`users.db`), active orders view, and real-time execution log streaming.
- **Pagination-Aware Historical Fetcher**: Robust bar-by-bar backtester capable of paginating up to 72,000+ candles across 250+ days within exchange rate limits, with zero lookahead bias.

#### 🛠️ Tech Stack
- **Core Engine**: Python 3.11+, `ccxt`, `asyncio`, NumPy, Pandas
- **Storage & Auth**: SQLite, Storage Adapter, Argon2 / PBKDF2 password hashing, session tokens
- **Monitoring & Interface**: Vanilla JavaScript Glassmorphic UI, Server-Sent Events / REST, WebSockets
- **Testing**: `pytest`, synthetic scenario fuzzing, mock exchange sandboxes

🔗 **Repository**: [https://github.com/Podugboch/BOT](https://github.com/Podugboch/BOT)

---

### 2. 🌐 [Nesty — Real-Time WebRTC Calling, Social Video Reels & Community Platform](https://github.com/Podugboch/Nesty)

[![Repository](https://img.shields.io/badge/GitHub-Podugboch%2FNesty-181717?style=flat-square&logo=github)](https://github.com/Podugboch/Nesty)
[![Backend](https://img.shields.io/badge/Backend-Go%201.25%20%7C%20Gin-00ADD8?style=flat-square&logo=go&logoColor=white)](https://golang.org)
[![Frontend](https://img.shields.io/badge/Frontend-React%2019%20%7C%20TypeScript-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![WebRTC](https://img.shields.io/badge/Calling-WebRTC%201080p-333333?style=flat-square&logo=webrtc)](https://webrtc.org)
[![Scaling](https://img.shields.io/badge/Concurrency-100k%20Users%20Scale-success?style=flat-square)](#)
[![Live Demo](https://img.shields.io/badge/Live%20Deployment-Render-46E3B7?style=flat-square&logo=render)](https://piscine-devnest.onrender.com)

> **Next-generation, high-concurrency real-time social platform engineered to handle 100,000 concurrent users. Unites peer-to-peer 1080p WebRTC calling, short-form video reels with dual audio mixing, live broadcast streaming, anti-spam community channels, and direct messaging.**

#### 📐 Core Architecture & Real-Time Engineering
1. **Ultra-Low Latency Calling Engine**: WebRTC peer-to-peer 1-on-1 audio/video calls, embedded community group conferencing with multi-track mesh broadcasting, dynamic renegotiation, screen sharing, and Coturn STUN/TURN NAT traversal.
2. **Native Mobile Integration (Android & iOS)**: Packaged with Capacitor; features native Android lock-screen takeover via `TelecomManager`, foreground `CallStyle` notifications, and native incoming call screens alongside iOS CallKit readiness.
3. **Short-Form Video Reels Engine**: Full-screen vertical swipe feed with gesture physics, Jamendo royalty-free soundtrack licensing, dual audio mixer (original video volume + soundtrack audio balance), and synchronized slide-up comment drawer.
4. **Live Broadcast Studio**: Broadcaster interface supporting camera streaming, real-time screen sharing, interactive live chat streams, and audience participant tracking.
5. **Anti-Spam Community System**: Role-based channel permissions (Creator, Admin, Co-Admin, Member) where users only see channels they own or are invited to, with invite validation workflows.
6. **Distributed Scaling**: Horizontal multi-container WebSocket clustering powered by Redis Pub/Sub, connection-pooled PostgreSQL with GORM, and S3-compatible cloud storage for binary media assets.

#### 🛠️ Tech Stack
- **Backend**: Go (Golang) 1.25, Gin Framework, Gorilla WebSocket, GORM
- **Frontend**: React 19, TypeScript, Vite, Web Audio & Canvas APIs, CSS3 Variables
- **Database & Cache**: PostgreSQL (Supabase), Redis (Pub/Sub & Key-Value clustering)
- **Mobile & Media**: Capacitor, Android Native Java/Kotlin Services, Supabase Storage, Jamendo API
- **DevOps**: Multi-stage Dockerfile, Alpine Linux, Render Web Services

🚀 **Live App**: [https://piscine-devnest.onrender.com](https://piscine-devnest.onrender.com)  
🔗 **Repository**: [https://github.com/Podugboch/Nesty](https://github.com/Podugboch/Nesty)

---

### 3. 🧭 [Auram — TravReady: AI Personal Office Assistant & Travel Intelligence](https://github.com/Podugboch/auram)

[![Repository](https://img.shields.io/badge/GitHub-Podugboch%2Fauram-181717?style=flat-square&logo=github)](https://github.com/Podugboch/auram)
[![Frontend](https://img.shields.io/badge/Frontend-React%2019%20%7C%20TypeScript-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![AI Model](https://img.shields.io/badge/AI%20Engine-Google%20Gemini%20Flash-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)](https://ai.google.dev)
[![Mobile](https://img.shields.io/badge/Mobile-Android%20APK%20%7C%20Capacitor-A4C639?style=flat-square&logo=android&logoColor=white)](https://github.com/Podugboch/auram/releases)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Vercel-black?style=flat-square&logo=vercel)](https://temporary-prompt-obsidian-rr1pbs6.vercel.app)

> **An AI-native autonomous personal office and travel intelligence assistant built on a zero-hardcoded location architecture, pairing generative AI with live geospatial telemetry and curated African hospitality experiences.**

#### 📐 Core Architecture & Intelligence Pipeline
1. **Zero-Hardcoded Location Architecture**: Dynamically acquires hardware GPS and network telemetry (`navigator.geolocation`), performing live reverse-geocoding via OpenStreetMap Nominatim and BigDataCloud.
2. **Dual-Mode Conversational AI**: Live Google Gemini integration (`gemini-3.6-flash`, `gemini-3.8-flash`) grounded with real-time telemetry, location coordinates, schedule items, and user context. Features automatic fallback to an in-memory rule-based NLP engine for seamless offline execution.
3. **Office Workspace & Natural Language Quick-Add**: Automated NLP parser extracting dates, times, priority, and venues from unstructured conversational inputs (*"Schedule sync with engineering lead at 2pm tomorrow"*).
4. **Microclimate Forecasting & Routing Corridor**: Real-time Open-Meteo meteorological forecasting for exact GPS coordinates, interactive Leaflet point-to-point route mapping, and 4-step progressive travel planning with dynamic packing checklists.
5. **African Hospitality Curation**: Curated directories of premier hospitality, dining, and executive workspaces across Lagos, Abuja, Accra, Nairobi, and Kigali.
6. **Cross-Platform Delivery**: Native Android deployment (`com.travready.app`) built with Capacitor, automated CI/CD compiling debug APKs via GitHub Actions on every push, and progressive web app (PWA) installation.

#### 🛠️ Tech Stack
- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS, Lucide Icons
- **AI & NLP**: Google Gemini API, Custom Client NLP Engine, Streaming Markdown Parser
- **Geospatial & APIs**: Leaflet, OpenStreetMap Nominatim, Open-Meteo Weather API, BigDataCloud
- **Mobile & Storage**: Capacitor (Android native SDK), Supabase PostgreSQL, Vercel

🚀 **Live App**: [https://temporary-prompt-obsidian-rr1pbs6.vercel.app](https://temporary-prompt-obsidian-rr1pbs6.vercel.app)  
🔗 **Repository**: [https://github.com/Podugboch/auram](https://github.com/Podugboch/auram)

---

### 4. 🧹 [Cluster-4-Cleaning-Roster — Automated Duty Rotation & Live Countdown Engine](https://github.com/Podugboch/Cluster-4-Cleaning-Roster)

[![Repository](https://img.shields.io/badge/GitHub-Podugboch%2FCluster--4--Cleaning--Roster-181717?style=flat-square&logo=github)](https://github.com/Podugboch/Cluster-4-Cleaning-Roster)
[![Framework](https://img.shields.io/badge/Framework-TanStack%20Start%20%7C%20React%2019-FF4154?style=flat-square&logo=react)](https://tanstack.com/start)
[![Language](https://img.shields.io/badge/Language-TypeScript%205.8-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Styling](https://img.shields.io/badge/Styling-Tailwind%20CSS%204-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Deployment](https://img.shields.io/badge/Edge%20Deploy-Cloudflare%20Workers-F38020?style=flat-square&logo=cloudflare)](https://workers.cloudflare.com)

> **A real-time, synchronized facility maintenance and duty scheduling platform designed for collaborative workspaces and educational clusters, featuring deterministic rotation algorithms and sub-second live session countdowns.**

#### 📐 Core Architecture & System Logic
1. **Deterministic Rotation State Machine**: Cyclical duty scheduling algorithm synchronizing 10 team tables across bi-weekly cleaning sessions (every Monday and Thursday at 00:00 local time). Computes current, next, and historical table duties from an immutable timeline anchor.
2. **Sub-Second Reactive Countdown**: High-precision timer ticking every 1,000ms, displaying live days, hours, minutes, and seconds until the next duty handover.
3. **Dynamic State Badging**: Real-time status categorization (`onDuty`, `next`, `done`, `upcoming`) with visual badge cues, intuitive progress trackers, and table assignment cards.
4. **Zero-Latency Edge Architecture**: Built on modern **TanStack Start** and **TanStack Router**, leveraging Cloudflare Workers edge deployment with instant server-side hydration and asset minification.

#### 🛠️ Tech Stack
- **Framework & Routing**: TanStack Start, TanStack Router, React 19
- **Languages & Typing**: TypeScript 5.8+, Zod schema validation
- **Styling & UI**: Tailwind CSS 4, Radix UI primitives, Lucide Icons, Embla Carousel
- **Deployment & Tooling**: Cloudflare Workers (Wrangler), Vite 7, Bun runtime

🔗 **Repository**: [https://github.com/Podugboch/Cluster-4-Cleaning-Roster](https://github.com/Podugboch/Cluster-4-Cleaning-Roster)

---

## 🌟 Other Noteworthy Projects

| Project | Description | Primary Stack | Link |
| :--- | :--- | :--- | :--- |
| 🛡️ **ChainShield** | AI Anti-Phishing Scanner & Crypto Scam Forensics Platform | JavaScript, AI Heuristics, Web Security | [Repo](https://github.com/Podugboch/chainshield) |
| 📈 **Chief-Trader** | Algorithmic Market Scanner, Trend Analyzer & Execution Monitor | Python, Pandas, Financial APIs | [Repo](https://github.com/Podugboch/Chief-Trader) |
| 🎓 **STAC-Alumni-Connect** | Networking and community platform connecting alumni for mentorship and career opportunities | Full-Stack Web, PostgreSQL, REST APIs | [Repo](https://github.com/Podugboch/STAC-Alumni-Connect-) |
| ⚙️ **DocDecoder** | High-efficiency document forensic decoder and automated structural metadata parser | Go, Python, Shell | [Repo](https://github.com/Podugboch/docdecoder) |
| 🧪 **MyProject** | Exploratory low-level systems programming, memory management & network primitives | Go, C, Systems Tooling | [Repo](https://github.com/Podugboch/myproject) |

---

## 🛠️ Complete Technical Skill Matrix

```
┌─────────────────────────┬────────────────────────────────────────────────────────────────────────┐
│ DOMAIN                  │ TECHNOLOGIES & TOOLS                                                   │
├─────────────────────────┼────────────────────────────────────────────────────────────────────────┤
│ Languages               │ Go (Golang), Python, TypeScript, JavaScript, SQL, Bash / Shell, HTML5, CSS3 │
│ Backend & Systems       │ Gin, GORM, WebSockets (Gorilla), Asyncio, Redis Pub/Sub, REST APIs     │
│ Real-Time & Media       │ WebRTC (Mesh & P2P), Coturn STUN/TURN, Web Audio API, Canvas API       │
│ Frontend Frameworks     │ React 19, TanStack Start, TanStack Router, Vite, Tailwind CSS 4, Radix  │
│ Mobile Engineering      │ Capacitor, Android SDK (Java/Kotlin), Native Notification Services     │
│ Cloud & DevOps          │ Docker, Cloudflare Workers, Render, Vercel, Supabase, Alpine Linux      │
│ Quantitative & AI       │ CCXT (100+ exchanges), Google Gemini API, Technical Indicators, NLP   │
│ Security & Fortification│ Zero-Trust Secret Handling, Kill Switches, Circuit Breakers, PBKDF2/Argon2 │
│ Tooling & Testing       │ Git, GitHub Actions CI/CD, PyTest, Bun, Linux System Administration   │
└─────────────────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## 📊 GitHub Analytics & Repository Metrics

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Podugboch&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true&cache_seconds=1800&v=2" alt="Patrick's GitHub Stats" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Podugboch&layout=compact&theme=tokyonight&hide_border=true&cache_seconds=1800&v=2" alt="Top Languages" width="48%" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Podugboch&theme=tokyonight&hide_border=true&cache_seconds=1800&v=2" alt="GitHub Streak" width="97%" />
</p>

---

## 🛡️ Fortification & Engineering Standards

All repositories under the **Podugboch** namespace follow strict production-grade hardening:

1. **Security-First Paradigm**:
   - Zero hardcoded credentials or API keys; all secrets are loaded dynamically through environment variables or secure secret managers.
   - Circuit breakers and graceful degradation built into all networked services (trading engines, WebSocket clusters, AI endpoints).
   - Responsible vulnerability disclosure process outlined in [`SECURITY.md`](SECURITY.md).
2. **Quality & Continuous Verification**:
   - Automated linting, link verification, and markdown structure validation via GitHub Actions ([`.github/workflows/validate.yml`](.github/workflows/validate.yml)).
   - Continuous dependency auditing with Dependabot ([`.github/dependabot.yml`](.github/dependabot.yml)).
3. **Open Collaboration**:
   - Transparent contribution workflows and code reviews governed by [`CONTRIBUTING.md`](CONTRIBUTING.md) and [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).
   - Standardized MIT open-source licensing ([`LICENSE`](LICENSE)).

---

## 🤝 Let's Connect & Build

Whether you are looking to collaborate on distributed systems, real-time protocols, algorithmic trading engines, or AI-native mobile apps, feel free to reach out:

<p align="center">
  <a href="https://www.linkedin.com/in/patrick-sean-odugboche-826115176"><img src="https://img.shields.io/badge/LinkedIn-Patrick%20Odugboche-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/Jaytricks35"><img src="https://img.shields.io/badge/X-@Jaytricks35-000000?style=for-the-badge&logo=x&logoColor=white" alt="Twitter / X" /></a>
  <a href="mailto:odu.pisc@gmail.com"><img src="https://img.shields.io/badge/Email-odu.pisc@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<p align="center">
  <sub>© 2026 Patrick Sean Odugboche • Built with engineering rigor, fortified against volatility.</sub>
</p>
