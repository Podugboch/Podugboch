# Security Policy

Patrick Sean Odugboche (`Podugboch`) takes security, reliability, and code integrity seriously across all repositories, open-source projects, and systems architectures.

---

## 🛡️ Supported Versions

Security updates and vulnerability remediation are actively maintained for the following branches:

| Project | Branch | Supported |
| :--- | :--- | :--- |
| **BOT** (Trader Queen) | `main` | :white_check_mark: Active |
| **Nesty** | `main` | :white_check_mark: Active |
| **Auram** (TravReady) | `main` | :white_check_mark: Active |
| **Cluster-4-Cleaning-Roster** | `main` | :white_check_mark: Active |
| **ChainShield** | `main` | :white_check_mark: Active |
| **Podugboch** (Profile & Meta) | `main` | :white_check_mark: Active |

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability, credential exposure, or exploit vector in any project under the `Podugboch` namespace, **please do not open a public GitHub issue.**

Instead, report it confidentially using one of the following methods:

1. **GitHub Private Security Advisory**: Use the "Report a vulnerability" button under the **Security** tab of the respective repository (if enabled).
2. **Direct Security Email**: Send details directly to:
   - **Primary Contact**: [odu.pisc@gmail.com](mailto:odu.pisc@gmail.com)
   - **Subject**: `[SECURITY VULNERABILITY] <Project Name> - <Brief Issue Description>`

### Please include the following details in your disclosure:
- Type and severity of the vulnerability (e.g., authentication bypass, injection, secret leak, race condition).
- Affected repository, branch, or release version.
- Step-by-step reproduction instructions or proof-of-concept (PoC) code.
- Potential impact and threat assessment.
- Any suggested remediations or mitigations.

---

## ⏱️ Response & Disclosure Timeline

- **Initial Acknowledgment**: Within **24 to 48 hours** of report receipt.
- **Triage & Assessment**: Within **3 to 5 business days**.
- **Fix & Patch Deployment**: Targeted within **7 to 14 business days**, depending on complexity.
- **Public Disclosure**: Coordinated disclosure after patches have been verified and deployed across production services.

---

## 🔒 Security Best Practices & Design Standards

All projects under the `Podugboch` organization adhere to the following principles:

1. **Zero Secret Leakage**:
   - No API keys, database credentials, JWT secrets, or exchange tokens are ever committed to version control.
   - All environments utilize `.env` files protected by `.gitignore` and platform secret managers.
2. **Circuit Breakers & Kill Switches**:
   - Algorithmic trading and financial tools incorporate filesystem/signal kill switches (`touch KILL`), maximum drawdown limits, and daily loss circuit breakers.
3. **Transport Security & Cryptography**:
   - All client-server communication enforces TLS 1.3 / HTTPS and WSS (secure WebSockets).
   - User credentials use secure password hashing algorithms (Argon2id, PBKDF2 with high iterations).
4. **Dependency Auditing**:
   - Regular automated scanning of dependencies for known CVEs via Dependabot and GitHub Security scanning.

Thank you for helping keep our software secure!
