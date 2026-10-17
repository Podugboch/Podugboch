# Contributing to Podugboch Repositories

First off, thank you for considering contributing! Projects under the **Podugboch** namespace are built with a commitment to engineering rigor, performance, and clean design.

---

## 🧭 Code of Conduct

All contributors and participants are expected to uphold our [Code of Conduct](CODE_OF_CONDUCT.md). Please report unacceptable behavior to [odu.pisc@gmail.com](mailto:odu.pisc@gmail.com).

---

## 🛠️ How to Contribute

### 1. Reporting Bugs
- Search existing issues to ensure the bug hasn't already been reported.
- Open a new issue with a clear title and detailed reproduction steps, environment details (OS, Go/Python/Node version), and expected vs. actual behavior.

### 2. Suggesting Features & Enhancements
- Open a feature proposal issue detailing the motivation, architectural implications, and user benefit before submitting large pull requests.

### 3. Pull Request Process
1. **Fork** the repository and create your feature branch:
   ```bash
   git checkout -b feat/your-feature-name
   ```
2. **Adhere to Code Standards**:
   - Write clean, idiomatic code (Go: `gofmt` & `golangci-lint`; Python: `ruff` or `black` + `pytest`; TypeScript: `prettier` & `eslint`).
   - Include automated tests for new functionality or bug fixes.
   - Maintain zero secret commits (never include `.env` or personal tokens).
3. **Commit Messages**: Follow Conventional Commits format:
   - `feat: add dynamic trailing stop in bot risk manager`
   - `fix: resolve WebRTC mesh connection teardown race condition`
   - `docs: update pinned repo specifications in profile`
4. **Submit PR**: Open a pull request against the `main` branch with a clear summary of changes.

---

## 🚀 Development Philosophy

- **Resilience**: Handle failures gracefully; don't let single errors crash background loops or WebSocket hubs.
- **Performance**: Benchmark hot code paths (e.g., kline processing in BOT, WebSocket broadcast in Nesty).
- **Simplicity**: Prefer clear, maintainable solutions over complex premature abstractions.

Thank you for contributing!
