<!-- ============================================================== -->
<!--   WorksheetJS · Security Policy  —  HTML-rendered             -->
<!-- ============================================================== -->

<a name="top"></a>

<p align="center">
  <img
    src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1020,40:7C3AED,100:A855F7&height=200&section=header&text=Security%20Policy&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=Private%20disclosure%20%C2%B7%20coordinated%20fixes%20%C2%B7%20BYO-key%20safety&descAlignY=62&descSize=12&animation=fadeIn"
    alt="WorksheetJS · Security Policy"
    width="100%"
  />
</p>

<p align="center">
  <img src="https://worksheetjs.com/images/worksheetjs-logo.png" alt="WorksheetJS" height="68" />
</p>

<h1 align="center">
  <img src="https://api.iconify.design/lucide:shield-check.svg?color=%237C3AED&width=28" align="center" />
  &nbsp;Security Policy
</h1>

<p align="center"><b>The security of WorksheetJS users — and the data they process in-browser — is our top priority.</b></p>

<p align="center">
  <a href="mailto:security@worksheetjs.com"><img alt="Email" src="https://img.shields.io/badge/security%40worksheetjs.com-private%20channel-7C3AED?style=for-the-badge&logo=maildotru&logoColor=white&labelColor=0b1020"></a>
  <a href="../../security/advisories/new"><img alt="GHSA" src="https://img.shields.io/badge/GitHub%20Security-Advisory-A855F7?style=for-the-badge&logo=github&logoColor=white&labelColor=0b1020"></a>
  <a href="https://worksheetjs.com/information-security-policy"><img alt="InfoSec policy" src="https://img.shields.io/badge/InfoSec-Policy-22c55e?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0b1020"></a>
</p>

<p align="center">
  <sub>
    <img src="https://api.iconify.design/lucide:sparkles.svg?color=%237C3AED&width=14" align="center" />
    &nbsp;How to report a vulnerability · what's in scope · how we handle AI / BYO-API-key risks&nbsp;
    <img src="https://api.iconify.design/lucide:sparkles.svg?color=%237C3AED&width=14" align="center" />
  </sub>
</p>

<br/>

<!-- ────────────  REPORTING  ──────────── -->

<h2>
  <img src="https://api.iconify.design/lucide:megaphone.svg?color=%237C3AED&width=22" align="center" />
  &nbsp;Reporting a vulnerability
</h2>

<blockquote>
  <p>
    <img src="https://api.iconify.design/lucide:alert-octagon.svg?color=%23ef4444&width=16" align="center" />
    &nbsp;<b>Caution.</b> <b>Please do not open a public GitHub issue for security problems.</b>
    Public disclosure before a patch puts users at risk.
  </p>
</blockquote>

<p>Use one of these private channels:</p>

<table width="100%">
  <thead>
    <tr><th align="left">Channel</th><th align="left">Use when</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://api.iconify.design/lucide:mail.svg?color=%237C3AED&width=16" align="center" />&nbsp; <b>Email:</b> <code>support@worksheetjs.com</code></td>
      <td>Default — all vulnerability reports</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:lock.svg?color=%23A855F7&width=16" align="center" />&nbsp; <b>GitHub Security Advisory</b></td>
      <td><a href="../../security/advisories/new">Report privately via GitHub</a></td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:briefcase.svg?color=%23f59e0b&width=16" align="center" />&nbsp; <b>Enterprise customers</b></td>
      <td>Your assigned support contact</td>
    </tr>
  </tbody>
</table>

<h3>
  <img src="https://api.iconify.design/lucide:clipboard-list.svg?color=%237C3AED&width=18" align="center" />
  &nbsp;What to include
</h3>

<p>A good report helps us triage in <b>hours</b> instead of <b>days</b>:</p>

<table width="100%">
  <tr>
    <td align="center" width="56"><img src="https://api.iconify.design/lucide:package.svg?color=%237C3AED&width=28" /></td>
    <td><b>Package + version</b><br/><sub>e.g., <code>@worksheet-js/core@2.4.1</code></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="https://api.iconify.design/lucide:zap.svg?color=%23ef4444&width=28" /></td>
    <td><b>Impact</b><br/><sub>What can an attacker do? (data leak, code execution, DoS, etc.)</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="https://api.iconify.design/lucide:flask-conical.svg?color=%2322c55e&width=28" /></td>
    <td><b>Reproduction steps</b><br/><sub>Minimal repro, ideally a <a href="https://stackblitz.com">StackBlitz</a> or code snippet</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="https://api.iconify.design/lucide:globe.svg?color=%23A855F7&width=28" /></td>
    <td><b>Environment</b><br/><sub>Browser, framework, build tool</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="https://api.iconify.design/lucide:handshake.svg?color=%23f59e0b&width=28" /></td>
    <td><b>Disclosure preferences</b><br/><sub>Credit name, embargo period, CVE request</sub></td>
  </tr>
</table>

<blockquote>
  <p>
    <img src="https://api.iconify.design/lucide:info.svg?color=%237C3AED&width=16" align="center" />
    &nbsp;<b>Note.</b> We acknowledge every report within <b>2 business days</b>.
  </p>
</blockquote>

<br/>

<!-- ────────────  RESPONSE PROCESS  ──────────── -->

<h2>
  <img src="https://api.iconify.design/lucide:timer.svg?color=%237C3AED&width=22" align="center" />
  &nbsp;Our response process
</h2>

<table width="100%">
  <thead>
    <tr><th align="left">Stage</th><th align="left">Target timeline</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=14" align="center" />&nbsp; Acknowledgement of receipt</td>
      <td>≤ 2 business days</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:stethoscope.svg?color=%237C3AED&width=14" align="center" />&nbsp; Initial severity assessment (CVSS)</td>
      <td>≤ 5 business days</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:refresh-cw.svg?color=%23A855F7&width=14" align="center" />&nbsp; Fix in progress → reporter updated</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:wrench.svg?color=%23ef4444&width=14" align="center" />&nbsp; Patch released (critical / high)</td>
      <td>≤ 14 days from confirmation</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:wrench.svg?color=%23f59e0b&width=14" align="center" />&nbsp; Patch released (medium / low)</td>
      <td>Next scheduled release</td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:megaphone.svg?color=%2322c55e&width=14" align="center" />&nbsp; Public advisory + CVE</td>
      <td>After patch ships + coordinated disclosure window</td>
    </tr>
  </tbody>
</table>

<blockquote>
  <p>
    <img src="https://api.iconify.design/lucide:handshake.svg?color=%237C3AED&width=14" align="center" />
    &nbsp;We follow a <b>90-day coordinated disclosure</b> window by default.
    We're happy to extend or shorten it in discussion with the reporter.
  </p>
</blockquote>

<br/>

<!-- ────────────  SCOPE  ──────────── -->

<h2>
  <img src="https://api.iconify.design/lucide:target.svg?color=%237C3AED&width=22" align="center" />
  &nbsp;Scope
</h2>

<table width="100%">
  <tr>
    <th width="50%">
      <img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=18" align="center" />
      &nbsp;In scope
    </th>
    <th width="50%">
      <img src="https://api.iconify.design/lucide:circle-x.svg?color=%23ef4444&width=18" align="center" />
      &nbsp;Out of scope
    </th>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li><img src="https://api.iconify.design/lucide:package.svg?color=%237C3AED&width=14" align="center" />&nbsp; Current <b>major version</b> of any published <code>@worksheet-js/*</code> package</li>
        <li><img src="https://api.iconify.design/lucide:history.svg?color=%23A855F7&width=14" align="center" />&nbsp; The <b>previous major version</b>, for 6 months after a new major</li>
        <li><img src="https://api.iconify.design/lucide:file-text.svg?color=%2322c55e&width=14" align="center" />&nbsp; XLSX / CSV / HTML / JSON parsers — XXE, zip-slip, prototype pollution, etc.</li>
        <li><img src="https://api.iconify.design/lucide:function-square.svg?color=%23f59e0b&width=14" align="center" />&nbsp; Formula engine — sandbox escapes, infinite-loop DoS, unsafe evaluation</li>
        <li><img src="https://api.iconify.design/lucide:image.svg?color=%237C3AED&width=14" align="center" />&nbsp; Canvas renderer — info disclosure across iframes / origins</li>
        <li><img src="https://api.iconify.design/lucide:bot.svg?color=%23A855F7&width=14" align="center" />&nbsp; AI Copilot plugin — prompt injection leading to data exfil or unintended API calls</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; Issues in <b>unsupported old versions</b> — please upgrade first</li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; Vulnerabilities in your <b>own application code</b></li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; Missing security headers on the <a href="https://worksheetjs.com">worksheetjs.com</a> marketing site (still email us, but not treated as a package vuln)</li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; <b>Social engineering</b> or physical attacks</li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; <b>Denial of service</b> via extremely large files on the client — by design, limits are your app's responsibility</li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; Attacks requiring a <b>malicious browser extension</b> or compromised device</li>
        <li><img src="https://api.iconify.design/lucide:ban.svg?color=%2394a3b8&width=14" align="center" />&nbsp; Self-XSS (attacker must trick user into pasting code into devtools)</li>
      </ul>
    </td>
  </tr>
</table>

<br/>

<!-- ────────────  AI MODEL  ──────────── -->

<h2>
  <img src="https://api.iconify.design/lucide:bot.svg?color=%237C3AED&width=22" align="center" />
  &nbsp;AI Copilot — security model
</h2>

<p>The AI Copilot ships with intentional design choices you should know about.</p>

<h3>
  <img src="https://api.iconify.design/lucide:key-round.svg?color=%237C3AED&width=18" align="center" />
  &nbsp;Your API key, your control
</h3>

<ul>
  <li>The AI Copilot uses <b>your own API key</b> (OpenAI, Anthropic, Gemini, …). We never proxy AI traffic through our servers.</li>
  <li>Keys live in <b>your app's runtime</b> — keep them on your <b>backend</b> and proxy requests, rather than shipping them to the browser.</li>
  <li>If you must expose a key in the browser (demos, sandboxes), use <b>short-lived, rate-limited keys</b>.</li>
</ul>

<h3>
  <img src="https://api.iconify.design/lucide:database.svg?color=%23A855F7&width=18" align="center" />
  &nbsp;Data handling
</h3>

<ul>
  <li>Spreadsheet data is processed <b>entirely in the browser</b>. It does not transit our servers.</li>
  <li>When the AI Copilot is invoked, the <b>cell range you call it on</b> is sent to your chosen AI provider. No other sheet data is sent unless you explicitly enable cross-sheet context.</li>
  <li>
    <img src="https://api.iconify.design/lucide:eye-off.svg?color=%2322c55e&width=14" align="center" />
    &nbsp; <b>Privacy Mode</b> (see docs) redacts values before sending to the model, replacing them with placeholders.
  </li>
</ul>

<h3>
  <img src="https://api.iconify.design/lucide:alert-triangle.svg?color=%23f59e0b&width=18" align="center" />
  &nbsp;Prompt injection
</h3>

<ul>
  <li>Treat AI output as <b>untrusted</b> — like any other user input.</li>
  <li>
    <img src="https://api.iconify.design/lucide:circle-x.svg?color=%23ef4444&width=14" align="center" />
    &nbsp; Do not feed raw AI output into <code>eval</code>, <code>Function()</code>, or server-side code paths without review.
  </li>
  <li>
    <img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=14" align="center" />
    &nbsp; Validate AI-generated formulas / scripts before applying them programmatically.
  </li>
</ul>

<br/>

<!-- ────────────  SUPPLY CHAIN  ──────────── -->

<h2>
  <img src="https://api.iconify.design/lucide:link.svg?color=%237C3AED&width=22" align="center" />
  &nbsp;Supply-chain integrity
</h2>

<table width="100%">
  <thead>
    <tr><th align="left">Practice</th><th align="center">Status</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://api.iconify.design/lucide:badge-check.svg?color=%237C3AED&width=14" align="center" />&nbsp; Published with <b>npm provenance</b> (<a href="https://docs.npmjs.com/generating-provenance-statements">docs</a>)</td>
      <td align="center"><img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=18" /></td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:signature.svg?color=%23A855F7&width=14" align="center" />&nbsp; Releases signed and built from a protected CI pipeline</td>
      <td align="center"><img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=18" /></td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:file-text.svg?color=%2322c55e&width=14" align="center" />&nbsp; <b>SBOM</b> shipped with each release (on website changelog)</td>
      <td align="center"><img src="https://api.iconify.design/lucide:circle-check-big.svg?color=%2322c55e&width=18" /></td>
    </tr>
    <tr>
      <td><img src="https://api.iconify.design/lucide:siren.svg?color=%23ef4444&width=14" align="center" />&nbsp; Tampered or unexpected versions — <b>report immediately</b> via the channels above</td>
      <td align="center"><img src="https://api.iconify.design/lucide:alert-triangle.svg?color=%23f59e0b&width=18" /></td>
    </tr>
  </tbody>
</table>

<br/>

<!-- ────────────  FOOTER  ──────────── -->

<p align="center">
  <img
    src="https://capsule-render.vercel.app/api?type=waving&color=0:A855F7,100:0b1020&height=120&section=footer&text=Disclose%20responsibly.%20Ship%20safely.&fontSize=13&fontColor=ffffff&fontAlignY=70&animation=fadeIn"
    alt="Footer"
    width="100%"
  />
</p>

<p align="center">
  <sub><b>
    <img src="https://api.iconify.design/lucide:heart-handshake.svg?color=%23A855F7&width=14" align="center" />
    &nbsp;Thank you for helping keep WorksheetJS and its users safe.
  </b></sub><br/>
  <sub>
    <a href="https://worksheetjs.com">worksheetjs.com</a> ·
    <a href="./SUPPORT.md">support</a> ·
    <a href="./CODE_OF_CONDUCT.md">code of conduct</a>
  </sub>
</p>
