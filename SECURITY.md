# Security Policy

**Organisation:** Braee Organisation (Cormac Wilson)
**Applies to:** Portal · Simmer · Vault
**Last Updated:** June 2026

---

## Supported Versions

Only the latest version on the `main` branch is actively maintained and receives security updates. Older releases are not supported.

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities via public GitHub Issues.**

If you discover a vulnerability, please use GitHub's private vulnerability reporting:

1. Go to the affected repository on GitHub
2. Click the **Security** tab
3. Select **Report a vulnerability**
4. Provide as much detail as possible

Alternatively, contact the maintainer directly via GitHub: [@cormacwilson](https://github.com/cormacwilson)

### What to Include

- A description of the vulnerability and its potential impact
- Steps to reproduce the issue
- The affected application (Portal, Simmer, or Vault)
- Any proof-of-concept code or screenshots

---

## Response Timeline

| Step | Timeframe |
|---|---|
| Acknowledgement | Within 72 hours |
| Confirmation & triage | Within 7 days |
| Fix deployed | Within 30 days (critical issues within 7 days) |

---

## Security Practices

- Passwords hashed with **Argon2** — never stored in plain text
- JWTs stored in **HTTP-only, Secure, SameSite** cookies scoped to `.braeeorganisation.co.uk`
- Financial data in Vault **encrypted at rest**
- Bank credentials **never handled** by Vault — delegated entirely to the Open Banking provider via OAuth 2.0
- All secrets stored in **environment variables** — never hardcoded
- Dependencies regularly audited via `npm audit`
- **HTTPS** enforced across all subdomains via Apache and Let's Encrypt

---

## Recognition

Valid, responsibly disclosed vulnerabilities will be credited in the relevant GitHub Security Advisory (with your permission). Thank you for helping keep Braee Organisation web applications & services secure.
