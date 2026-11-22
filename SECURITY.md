# Security Policy

## Security Architecture

**Auditory Atlas** is a self-contained static web application hosted on GitHub Pages with:
- **Zero backend, database, or user accounts** — favorites, UI preferences, and personal notes remain exclusively in your browser's local storage and can be erased anytime inside **Theme & Info → Clear saved favorites & notes**.
- **Zero external runtime scripts, stylesheets, fonts, CDNs, or analytics** — no third-party telemetry or dependency supply-chain execution in the browser.
- **Strict hash-pinned Content Security Policy (`default-src 'none'`)** via `<meta http-equiv="Content-Security-Policy">`, `<meta name="referrer" content="no-referrer">`, strict URL/ORCID/DOI protocol allowlists, `rel="noopener noreferrer"` on all external links, and CSV formula-injection neutralization on exports.
- **Public-metadata boundary** — only publicly available institutional pages and public bibliometric records (OpenAlex, Europe PMC, ORCID) are included; private personal email addresses of PIs are intentionally excluded.

> **Hosting note on HTTP framing headers:** Static GitHub Pages (`build_type: legacy`) does not allow configuring `X-Frame-Options` or HTTP-header `CSP frame-ancestors`. All other browser CSP protections (`script-src`, `style-src`, `connect-src`, `base-uri`, `form-action`) are enforced in strict hash-pinned mode.

## Reporting a Vulnerability or Hijacked Link

Please report any security concern **privately** rather than opening a public issue:
- **GitHub Private Vulnerability Reporting:** Use the **Security → Advisories → Report a vulnerability** button in this repository (`https://github.com/Simoncio-art/auditory-labs-atlas/security/advisories/new`).

In scope:
- Cross-site scripting (XSS), CSP bypasses, or DOM injection vectors in `index.html`.
- Compromised, expired, hijacked, or phishing `lab_url` / `careers_url` external links.
- Fraudulent mirror/clone domains impersonating **Auditory Atlas**.
- Unintended exposure of personal data or non-public metadata.

For non-sensitive broken links or routine academic corrections, you may use the [Security / Broken Link Issue Form](https://github.com/Simoncio-art/auditory-labs-atlas/issues/new?template=security_or_broken_link.yml).
