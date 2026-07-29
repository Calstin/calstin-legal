# Security & Responsible Disclosure

**Calstin Software Solutions Inc.**

---

## Reporting a Vulnerability

If you discover a security vulnerability in Calstin, please report it responsibly. We take all reports seriously and will respond promptly.

**Email:** [security@calstin.com](mailto:security@calstin.com)

Please **do not** file a public GitHub issue for security vulnerabilities. Public disclosure before a fix is in place puts users at risk.

---

## What to Include in Your Report

A good report helps us triage and fix the issue faster. Please include:

- **Description** — what the vulnerability is and where it exists
- **Impact** — what an attacker could do by exploiting it
- **Steps to reproduce** — a clear, minimal reproduction path
- **Proof of concept** — screenshots, logs, or a PoC script if applicable
- **Suggested fix** — optional, but appreciated

---

## Our Commitment to You

- We will acknowledge receipt of your report within **2 business days**
- We will provide a status update within **7 business days**
- We will notify you when the vulnerability is patched
- We will credit you in our changelog if you wish (opt-in)
- We will not take legal action against researchers who act in good faith

---

## Scope

### In Scope

| Target | Description |
|--------|-------------|
| `calstin.com` | Main web platform |
| `calstin.com/api/*` | Public API endpoints |
| Wallet authentication flow | Sign-in challenge/response mechanism |
| Session management | Token issuance, expiry, revocation |
| Desktop application | Electron-based launcher |

### Out of Scope

| Item | Reason |
|------|--------|
| Third-party games | We don't control them — report directly to the game developer |
| Blockchain networks (Solana, Ethereum, etc.) | Out of our control |
| Social engineering attacks on Calstin staff | Out of scope for this program |
| Denial of service attacks | Please do not test this against production |
| Issues requiring physical access to a user's device | Out of scope |

---

## Vulnerability Classes We Care Most About

- Authentication bypass or session hijacking
- Wallet signature replay or forgery
- Cross-site scripting (XSS) that could affect wallet interactions
- Server-side injection (SQLi, command injection, etc.)
- Insecure direct object reference (IDOR) on user data
- Improper access control on admin/owner endpoints
- Sensitive data exposure in API responses

---

## What We Will NOT Pay For

Calstin does not currently operate a paid bug bounty program. We offer:

- Public acknowledgment (opt-in) in our changelog
- Our genuine gratitude

If this changes, we will update this document.

---

## Security Practices

### What we do

- All traffic served over TLS 1.2+
- Security headers enforced on every response: `Content-Security-Policy`, `Strict-Transport-Security`, `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`, `Permissions-Policy`
- Session cookies flagged `HttpOnly`, `Secure`, `SameSite=Strict`
- Wallet private keys and seed phrases are never transmitted to or stored by Calstin — ever
- Dependencies scanned regularly for known vulnerabilities
- No "audited" claims — we do not claim a formal third-party audit unless one has been completed and the report is published

### What we do not do (yet)

- Formal third-party security audit (planned)
- Bug bounty program with monetary rewards (planned)
- SOC 2 certification (planned for enterprise tier)

---

## Disclosure Policy

We follow a **coordinated disclosure** model:

1. Reporter submits vulnerability privately to security@calstin.com
2. We acknowledge within 2 business days
3. We investigate and develop a fix
4. We deploy the fix
5. We notify the reporter
6. Public disclosure agreed upon with the reporter (typically 90 days from initial report, or sooner once patched)

---

## PGP Key

PGP encryption for sensitive reports is available on request. Email security@calstin.com to request our public key.

---

## Hall of Fame

Researchers who responsibly disclose valid vulnerabilities will be listed here (with their permission).

*No entries yet — be the first.*

---

## Contact

| Purpose | Contact |
|---------|---------|
| Security vulnerabilities | security@calstin.com |
| Privacy questions | privacy@calstin.com |
| Legal matters | legal@calstin.com |
| General | hello@calstin.com |
