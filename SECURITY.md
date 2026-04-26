<div align="center">

<img src="https://worksheetjs.com/images/worksheetjs-logo.png" alt="WorksheetJS" height="72" />

<h1>🔒 Security Policy</h1>

<p><b>The security of WorksheetJS users — and the data they process in-browser — is our top priority.</b></p>

<p>
  <a href="mailto:security@worksheetjs.com"><img alt="Email" src="https://img.shields.io/badge/%E2%9C%89%20security%40worksheetjs.com-private%20channel-7C3AED?style=for-the-badge&labelColor=0b1020"></a>
  <a href="../../security/advisories/new"><img alt="GHSA" src="https://img.shields.io/badge/%F0%9F%94%90%20GitHub%20Security-Advisory-A855F7?style=for-the-badge&labelColor=0b1020"></a>
  <a href="https://worksheetjs.com/information-security-policy"><img alt="InfoSec policy" src="https://img.shields.io/badge/%F0%9F%93%9C%20InfoSec-policy-22c55e?style=for-the-badge&labelColor=0b1020"></a>
</p>

<sub>✦ This document explains how to report a vulnerability, what's in scope, and how we handle AI / BYO-API-key risks. ✦</sub>

</div>

---

## 📣 Reporting a vulnerability

> [!CAUTION]
> **Please do not open a public GitHub issue for security problems.** Public disclosure before a patch puts users at risk.

Use one of these private channels:

| Channel | Use when |
|---|---|
| 📧 **Email:** `security@worksheetjs.com` | Default — all vulnerability reports |
| 🔐 **GitHub Security Advisory** | [Report privately via GitHub](../../security/advisories/new) |
| 💼 **Enterprise customers** | Your assigned support contact |

### 🧾 What to include

A good report helps us triage in **hours** instead of **days**:

1. 📦 **Package + version** (e.g., `@worksheet-js/core@2.4.1`)
2. 💥 **Impact** — what can an attacker do? (data leak, code execution, DoS, etc.)
3. 🧪 **Reproduction steps** — minimal repro, ideally a [StackBlitz](https://stackblitz.com) or code snippet
4. 🌐 **Environment** — browser, framework, build tool
5. 🤝 **Your disclosure preferences** — credit name, embargo period, CVE request

> [!NOTE]
> We acknowledge every report within **2 business days**.

---

## ⏱ Our response process

| Stage | Target timeline |
|---|---|
| ✅ Acknowledgement of receipt | ≤ 2 business days |
| 🩺 Initial severity assessment (CVSS) | ≤ 5 business days |
| 🔄 Fix in progress → reporter updated | Weekly |
| 🛠 Patch released (critical / high) | ≤ 14 days from confirmation |
| 🛠 Patch released (medium / low) | Next scheduled release |
| 📢 Public advisory + CVE | After patch ships + coordinated disclosure window |

> 🤝 We follow a **90-day coordinated disclosure** window by default. We're happy to extend or shorten it in discussion with the reporter.

---

## 🎯 Scope

<table>
<tr>
<th width="50%">✅ In scope</th>
<th width="50%">❌ Out of scope</th>
</tr>
<tr>
<td valign="top">

- 📦 Current **major version** of any published `@worksheet-js/*` package
- 🕰 The **previous major version**, for 6 months after a new major
- 📄 XLSX / CSV / HTML / JSON parsers — XXE, zip-slip, prototype pollution, etc.
- 🧮 Formula engine — sandbox escapes, infinite-loop DoS, unsafe evaluation
- 🖼 Canvas renderer — info disclosure across iframes / origins
- 🤖 AI Copilot plugin — prompt injection leading to data exfil or unintended API calls

</td>
<td valign="top">

- 🚫 Issues in **unsupported old versions** — please upgrade first
- 🚫 Vulnerabilities in your **own application code**
- 🚫 Missing security headers on the [worksheetjs.com](https://worksheetjs.com) marketing site (still email us, but not treated as a package vuln)
- 🚫 **Social engineering** or physical attacks
- 🚫 **Denial of service** via extremely large files on the client — by design, limits are your app's responsibility
- 🚫 Attacks requiring a **malicious browser extension** or compromised device
- 🚫 Self-XSS (attacker must trick user into pasting code into devtools)

</td>
</tr>
</table>

---

## 🧠 AI Copilot — security model

The AI Copilot ships with intentional design choices you should know about.

### 🔑 Your API key, your control

- The AI Copilot uses **your own API key** (OpenAI, Anthropic, Gemini, …). We never proxy AI traffic through our servers.
- Keys live in **your app's runtime** — keep them on your **backend** and proxy requests, rather than shipping them to the browser.
- If you must expose a key in the browser (demos, sandboxes), use **short-lived, rate-limited keys**.

### 📊 Data handling

- Spreadsheet data is processed **entirely in the browser**. It does not transit our servers.
- When the AI Copilot is invoked, the **cell range you call it on** is sent to your chosen AI provider. No other sheet data is sent unless you explicitly enable cross-sheet context.
- 🕶 **Privacy Mode** (see docs) redacts values before sending to the model, replacing them with placeholders.

### 🪤 Prompt injection

- Treat AI output as **untrusted** — like any other user input.
- 🚫 Do not feed raw AI output into `eval`, `Function()`, or server-side code paths without review.
- ✅ Validate AI-generated formulas / scripts before applying them programmatically.

---

## 🛡 Supply-chain integrity

| Practice | Status |
|---|:---:|
| 📜 Published with **npm provenance** ([docs](https://docs.npmjs.com/generating-provenance-statements)) | ✅ |
| ✍ Releases signed and built from a protected CI pipeline | ✅ |
| 🧾 **SBOM** (Software Bill of Materials) shipped with each release (on website changelog) | ✅ |
| 🚨 Tampered or unexpected versions — **report immediately** via the channels above | ⚠️ |

---

## 🏅 Hall of Fame

We publicly **credit researchers** who report valid vulnerabilities (unless you prefer to stay anonymous). Credits appear in the release notes and security advisories for the fix.

> 💰 We don't currently run a paid bug bounty, but **enterprise customers** may sponsor bounties for specific scopes — reach out via `security@worksheetjs.com`.

---

## 📎 Further reading

- 🔗 [OWASP Top 10 — Web Application Security Risks](https://owasp.org/Top10/)
- 🔗 [CVSS v3.1 Calculator](https://www.first.org/cvss/calculator/3.1)
- 🔗 [WorksheetJS Information Security Policy](https://worksheetjs.com/information-security-policy)

---

<div align="center">

<sub><b>🙏 Thank you for helping keep WorksheetJS and its users safe.</b></sub><br/>
<sub><a href="https://worksheetjs.com">worksheetjs.com</a> · <a href="./SUPPORT.md">support</a> · <a href="./CODE_OF_CONDUCT.md">code of conduct</a></sub>

</div>
