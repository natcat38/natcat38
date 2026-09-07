# Natalie Yap

Full-stack engineer — backend systems, real-time services, and developer-facing tools.

I build and ship things end-to-end: production experience across TypeScript/React/Next.js,
Go, and Python, with Temporal, GraphQL, and PostgreSQL. I care about clear architecture,
software that's actually used, and shipping in the open.

**Open to software engineering roles in Singapore.**

---

### [invoicely](https://github.com/natcat38/invoicely) — [live demo](https://invoicely-loo1.onrender.com)

Maker-checker invoicing for a small Singapore business: staff draft invoices, only the owner approves, sends, and records payments — a split enforced in the API, not just hidden in the UI. *(Log in as `owner@invoicely.demo` or `staff@invoicely.demo`, password `invoicely-demo-2026`; the free instance takes ~30 s to wake on first load.)*

Java 25 / Spring Boot 4 with a React/TypeScript front end. Money is `BigDecimal` rounded in exactly one place, GST is snapshotted at send so a rate change never rewrites a document a client holds, and 150 tests run against a real PostgreSQL — including two payments racing to overpay one invoice and two invoices racing for the same number. Every non-obvious decision is a written ADR.

### [rpg-build-optimizer](https://github.com/natcat38/rpg-build-optimizer) — [live demo](https://rpg-build-optimizer.vercel.app)

Finds the optimal five-piece Genshin Impact artifact build from an inventory of hundreds of items, entirely in the browser.

The search is exact branch-and-bound, not a heuristic: on an 800-artifact inventory it explores roughly 1 in 89,043 of the ~105 billion possible builds, and a brute-force oracle run over randomised inventories proves the pruning never discards the true optimum.

### [f1-race-tracker](https://github.com/natcat38/f1-race-tracker) — [static demo](https://natcat38.github.io/f1-race-tracker/)

A pit-wall view of an F1 session: cars on the track map, live timing tower, telemetry, and strategy, updating at 10 Hz. *(The demo is a frontend-only replay of one recorded clip — the full polyglot stack runs via Docker Compose.)*

Python ingest and a Go writer publish byte-identical JSON to Redis as a language-agnostic seam, and a Go gateway fans those frames out over WebSocket — benchmarked at 1,000 concurrent viewers with p99 fan-out of 48 ms and zero dropped clients.

### [trip-planner](https://github.com/natcat38/trip-planner) — [shared itinerary](https://trip-planner-cyan-five.vercel.app/shared/OHLsGOqKXdyIirGnwTDRr0YemWKKDpbK)

A multi-user planner for long, multi-city trips: day-by-day itinerary, a budget that tracks spending across currencies, and a map that stays in sync with the plan. *(The link is a real trip published through the app's read-only share route — no sign-in needed.)*

Money is stored as integer minor units with an ISO 4217 code and converted only on read, and every trip is reached through one of three explicit access gates — owner, accepted collaborator, or anonymous share token — so the public route can't leak a field the owner didn't publish.

---

### Tech I work with

**Languages** TypeScript · Go · Python · Java
**Frontend** React · Next.js · Tailwind
**Backend** Node · Spring Boot · GraphQL · Temporal · REST
**Data** PostgreSQL
**Payments** KiplePay · Sarawak Pay · CommercePay

---

### Links

[LinkedIn](https://www.linkedin.com/in/natalie-yap-eng) · [Email](mailto:natalieyap38@outlook.com)
