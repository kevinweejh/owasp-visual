# 🛡️ OWASP Top 10 — Visualised (2025 Edition)

**A static, interactive educational site that shows web developers what OWASP Top 10 vulnerabilities actually look like** — from the vulnerable code, through the database, to what an attacker sees in Chrome DevTools.

Unlike hacking playgrounds (Juice Shop, WebGoat) where you exploit a live app, this project is a **visual museum exhibit**: step-by-step walkthroughs that show the anatomy of each vulnerability using simulated, static demonstrations. No setup, no Docker, no attack infrastructure.

> 🎯 **Target audience:** Web developers who write code daily and want to understand the _shape_ of security vulnerabilities without needing a penetration testing background.

---

## Viewing it

Open [OWASP Top 10 (2025) Visualised](https://labs.codebykevin.dev/owasp-visual/) in any modern browser. That's it — no build, no server, no dependencies.

Each vulnerability (A01–A10) walks through the same 5-step story: the normal flow, the vulnerable code, the attack, the impact, and the fix — shown from multiple perspectives (code, database, DevTools, fixed code, defense principles). Dark/light theming follows your OS setting by default, with a manual toggle to override.

---

## Content Coverage

Each category's "Impact" step also cites 2–3 verified real-world breaches illustrating that failure mode in practice.

| # | Category | Attack Vectors Demonstrated |
|---|----------|----------------------------|
| **A01** | Broken Access Control | IDOR via console fetch, SSRF via AWS metadata, automated enumeration script |
| **A02** | Security Misconfiguration | Default credentials, verbose error messages, open S3 buckets, CORS wildcard, header leakage, Nuclei scanning |
| **A03** | Software Supply Chain Failures | Dependency trees, typosquatting, CI/CD pipeline poisoning, Log4Shell exploitation, lock file reconnaissance |
| **A04** | Cryptographic Failures | Unsalted MD5 password hashing, rainbow table lookup, offline hashcat cracking |
| **A05** | Injection | SQL injection via string concatenation, UNION-based data extraction, stored XSS cookie theft |
| **A06** | Insecure Design | Guessable security-question password reset, OSINT-based account takeover, brute-forced recovery flow |
| **A07** | Authentication Failures | Credential stuffing, MFA push-fatigue attack, unrestricted login attempts |
| **A08** | Software or Data Integrity Failures | Unsigned auto-update tampering, insecure Node.js deserialization RCE |
| **A09** | Logging & Alerting Failures | Alerts routed to unmonitored channels, signal buried in high-volume logs |
| **A10** | Mishandling of Exceptional Conditions | ReDoS via catastrophic regex backtracking, single-threaded event-loop exhaustion |

---

## Architecture

Three files, no build step, no framework: `index.html` (all content), `styles.css` (theming + a reusable "mock UI" component library), `script.js` (a single `DOMContentLoaded` handler wiring up all interactivity).

---

## License & Disclaimer

### Disclaimer

This project is an **educational resource** for defensive security awareness. All demonstrations use simulated, static examples. No real systems are targeted, attacked, or harmed.

The techniques shown are for **defensive understanding only** — to help developers recognise, prevent, and fix these issues in their own code.

**Unauthorised testing of systems you do not own is illegal** under:
- Computer Fraud and Abuse Act (CFAA) — United States
- Computer Misuse Act 1990 — United Kingdom
- Equivalent legislation in most jurisdictions worldwide

### Attribution

- Based on the [OWASP Top 10 (2025)](https://owasp.org/Top10/) by the OWASP Foundation
- Not affiliated with or endorsed by the OWASP Foundation
- Real-world breach examples cited for educational context only

### License

MIT License — see [LICENSE](LICENSE) for details.

---

<p align="center">
  <strong>Built with 🛡️ by a web developer learning security — for web developers learning security.</strong>
</p>
