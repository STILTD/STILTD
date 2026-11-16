# KYO INC (STILTD)

KYO INC is a small software engineering team. Our goal is to make digital environments safer, bit by bit. We do that by building our own software with security treated as part of the work, and by fixing the gaps we find in it as we go.

---

## What We Do

We build and maintain web applications and the services behind them. We also build the internal tools our own team runs on.

We test our own software the way an attacker would, find where it breaks, fix it, and record what we learned. We have shipped bugs and security flaws before. What we commit to is finding them early and fixing them properly.

---

## How We Build

- **Security is part of the code.** Authentication, permissions, input validation and encryption live inside the application logic. We don't rely only on a firewall or on the UI hiding buttons.
- **Least privilege by default.** Every role gets only the access it needs, and the server checks permissions even when the frontend already does.
- **We don't trust input.** Data from users, external APIs and AI models is validated before we use it. Database queries are parameterized. Outbound requests from our servers only go to approved domains.
- **We test fixes against a running system.** A security fix isn't finished because the code looks right. We reproduce the problem, apply the fix, and confirm the problem is gone in a live test.
- **We treat AI as an untrusted component.** Where we use AI models, they run inside the same permission rules as any user, and their output is checked before it's used.
- **We keep the code simple.** We favor readable, maintainable code over clever code, and we paginate data-heavy views so they stay fast on mobile.

---

## Languages & Tools

**Languages:** JavaScript (Node.js and browser), JSX, SQL, HTML and CSS.

**Frontend:** React, Vite, PixiJS (WebGL).

**Backend and infrastructure:** Node.js, Express, Cloudflare Workers and Pages, Docker.

**Databases and storage:** SQLite (including Cloudflare D1), PostgreSQL, Cloudflare R2.

**Security and identity:** Argon2id password hashing, AES-256-GCM encryption, WebAuthn passkeys, TOTP two-factor authentication, signed JWT sessions with revocation.

**Testing and review:** Our own attack-simulation and regression test scripts, GitHub CodeQL, Dependabot, and manual code review.

---

## What We Prioritize When Shipping

In this order:

1. **Security and correctness.** A feature that works but opens a hole doesn't ship.
2. **Verification.** Tests pass, the production build succeeds, and security changes are checked against a live run.
3. **Access control.** New features are checked for who can reach them and what they can see.
4. **Maintainability.** Another developer should be able to read it and change it safely.
5. **Performance.** It should be fast on weak devices and slow connections, not only on a developer machine.


---

## Reporting a Security Issue

Please don't open a public issue for a vulnerability. You can report directly to [@GABKYUd](https://github.com/GABKYUd

**Maintained by:** Gabriel Kyo ([@GABKYUd](https://github.com/GABKYUd))
