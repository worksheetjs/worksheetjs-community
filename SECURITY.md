# 🔒 Security Policy

The security of WorksheetJS users — and the data they process in-browser — is our top priority. This document explains **how to report a vulnerability**, **what's in scope**, and **how we handle AI and BYO-API-key risks** specifically.

---

## 📣 Reporting a vulnerability

**Please do not open a public GitHub issue for security problems.**

Use one of these private channels:

| Channel | Use when |
|---|---|
| 📧 **Email:** `security@worksheetjs.com` | Default — all vulnerability reports |
| 🔐 **GitHub Security Advisory** | [Report privately via GitHub](../../security/advisories/new) |
| 💼 **Enterprise customers** | Your assigned support contact |

### What to include

A good report helps us triage in hours instead of days:

1. **Package + version** (e.g., `@worksheet-js/core@2.4.1`)
2. **Impact** — what can an attacker do? (data leak, code execution, DoS, etc.)
3. **Reproduction steps** — minimal repro, ideally a [StackBlitz](https://stackblitz.com) or code snippet
4. **Environment** — browser, framework, build tool
5. **Your disclosure preferences** — credit name, embargo period, CVE request

We will acknowledge every report within **2 business days**.

---

## ⏱ Our response process

| Stage | Target timeline |
|---|---|
| Acknowledgement of receipt | ≤ 2 business days |
| Initial severity assessment (CVSS) | ≤ 5 business days |
| Fix in progress → reporter updated | Weekly |
| Patch released (critical / high) | ≤ 14 days from confirmation |
| Patch released (medium / low) | Next scheduled release |
| Public advisory + CVE | After patch ships + coordinated disclosure window |

We follow a **90-day coordinated disclosure** window by default. We're happy to extend or shorten it in discussion with the reporter.

---

## 🎯 Scope

### ✅ In scope

- Current **major version** of any published `@worksheet-js/*` package
- The **previous major version**, for 6 months after a new major is released
- XLSX / CSV / HTML / JSON parsers (file-handling bugs, XXE, zip-slip, prototype pollution, etc.)
- Formula engine (sandbox escapes, infinite-loop DoS, unsafe evaluation)
- Canvas renderer (information disclosure across iframes/origins)
- AI Copilot plugin (prompt injection leading to data exfiltration, unintended API calls)

### ❌ Out of scope

- Issues in **unsupported old versions** — please upgrade first
- Vulnerabilities in your **own application code** that happen to use our packages
- Missing security headers on [worksheetjs.com](https://worksheetjs.com) marketing site (report to `security@worksheetjs.com` but not treated as a package vuln)
- **Social engineering** or physical attacks
- **Denial of service** via extremely large files on the client — by design, limits are your app's responsibility
- Attacks requiring a **malicious browser extension** or compromised device
- Self-XSS (attacker must trick user into pasting code into devtools)

---

## 🧠 AI Copilot specific security model

The AI Copilot ships with design choices you should know about:

### Your API key, your control

- The AI Copilot uses **your own API key** (OpenAI, Anthropic, etc.). We never proxy AI traffic through our servers.
- Keys are stored in **your app's runtime** — we recommend you keep them on your backend and proxy requests, rather than shipping them to the browser.
- If you must expose a key in the browser (demos, sandboxes), use **short-lived, rate-limited keys**.

### Data handling

- Spreadsheet data is processed **entirely in the browser**. It does not transit our servers.
- When the AI Copilot is used, the **cell range you invoke it on** is sent to your chosen AI provider. No other sheet data is sent unless you enable cross-sheet context explicitly.
- **Privacy Mode** (see docs) redacts values before sending to the model, replacing them with placeholders.

### Prompt injection

- Treat AI output as **untrusted**. If you use the AI-generated formulas or scripts programmatically, validate them as you would any user input.
- Do not feed raw AI output into `eval`, `Function()`, or server-side code paths without review.

---

## 🛡 Supply-chain integrity

- All `@worksheet-js/*` packages are published with **npm provenance** ([docs](https://docs.npmjs.com/generating-provenance-statements))
- Releases are signed and built from a protected CI pipeline
- We publish an **SBOM** (Software Bill of Materials) with each release — available on the website changelog
- If you detect a tampered or unexpected package version, please report it immediately via the channels above

---

## 🏅 Hall of Fame

We publicly credit researchers who report valid vulnerabilities (unless you prefer to stay anonymous). Credits are listed in the release notes and security advisories for the fix.

We don't currently run a paid bug bounty, but enterprise customers may be able to sponsor bounties for specific scopes — reach out via `security@worksheetjs.com`.

---

## 📎 Further reading

- [OWASP Top 10 — Web Application Security Risks](https://owasp.org/Top10/)
- [CVSS v3.1 Calculator](https://www.first.org/cvss/calculator/3.1)
- [WorksheetJS Information Security Policy](https://worksheetjs.com/information-security-policy)

---

Thank you for helping keep WorksheetJS and its users safe. 🙏
