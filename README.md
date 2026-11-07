![header](https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=Hi%20there%20ツ&fontAlignY=45&animation=fadeIn)

<h1 align="center">Mostafa Saafan 👨‍💻</h1>

<p align="center">
  <b>Full-stack developer</b> building reliable SaaS products, AI assistants and interactive web experiences with React, Next.js, TypeScript, Node.js, PostgreSQL and Supabase.<br>
  Top Rated on Upwork with a 100% Job Success Score · Based in Egypt, working remotely with clients worldwide · Arabic and English
</p>

<p align="center">
  <a href="https://www.upwork.com/freelancers/~0104fa36ecdc4bf8a1"><img src="https://img.shields.io/badge/Hire%20me%20on-Upwork-14a800?style=for-the-badge&logo=upwork&logoColor=white" alt="Hire me on Upwork"></a>
  <a href="https://store-ops-mcp.mostafawork5517.workers.dev"><img src="https://img.shields.io/badge/Live-Store%20Ops%20MCP-0a0a0a?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Store Ops MCP live server"></a>
  <a href="https://hala-phi.vercel.app/demo"><img src="https://img.shields.io/badge/Live%20demo-Hala-0a0a0a?style=for-the-badge&logo=vercel&logoColor=white" alt="Hala live demo"></a>
  <a href="https://clubly-nine.vercel.app"><img src="https://img.shields.io/badge/Live%20demo-Clubly-0a0a0a?style=for-the-badge&logo=vercel&logoColor=white" alt="Clubly live demo"></a>
  <a href="https://sahra-khaki.vercel.app"><img src="https://img.shields.io/badge/Live%20demo-Sahra-0a0a0a?style=for-the-badge&logo=vercel&logoColor=white" alt="Sahra live demo"></a>
</p>

---

## What I do

- **AI assistants and agents:** answers grounded in a business's own data with sources (RAG), AI that can only act through validated server-side tools, evaluation suites that measure the AI's behavior, and cost tracking with spending limits.
- **MCP servers and Claude connectors:** remote MCP servers with OAuth sign-in, per-tool permissions, a human approval step before any change, audit logs, and interactive dashboards rendered inside Claude (MCP Apps).
- **Business automation:** AI workflows in n8n and Make.com that read email and forms, sort and extract data with AI, log to Google Sheets and draft replies for a human to approve, with retries and error handling.
- **SaaS products end to end:** multi-tenant apps, dashboards, authentication and roles, from the data model to production.
- **Payments that stay correct:** Stripe subscriptions and Stripe Connect, signed and idempotent webhooks, and reconciliation jobs, so no payment is ever lost or applied twice.
- **Secure data:** each customer's data isolated in the database itself with Postgres row-level security, plus append-only audit trails.
- **Taking over existing codebases,** including AI-built and low-code apps, and making them production-ready without rewriting what already works.
- **Interactive and animated front-end:** WebGL and Three.js scenes with custom shaders, scroll-driven animation with GSAP, and SVG animation, built to stay smooth on mid-range phones.
- **Mobile:** a React Native (Expo) app shipped to both the App Store and Google Play.
- **Testing and quality:** unit, database and Playwright end-to-end tests in CI, accessibility checks and Lighthouse performance.

## ⭐ Featured projects

### Store Ops MCP: a secure MCP server that connects Claude to an online store

**Lets a store owner run orders, products, stock and refunds by talking to Claude.** A remote MCP server on a demo store, with an interactive order dashboard that renders inside Claude.

🔗 **Live server:** [store-ops-mcp.mostafawork5517.workers.dev](https://store-ops-mcp.mostafawork5517.workers.dev) · 💻 **Code:** [github.com/MostafaSaafan5517/store-ops-mcp](https://github.com/MostafaSaafan5517/store-ops-mcp)

- **Remote MCP on Cloudflare Workers** with OAuth 2.1 sign-in (GitHub or a demo login) and per-tool scopes
- **Nothing changes without a human:** every write (stock, cancel, refund) needs an approval link bound to that exact action
- **Each store's data isolated** with Postgres row-level security on Neon, plus an append-only audit log of every change
- **Prompt-injection-safe:** store text such as product names and order notes is treated as data, never as instructions
- **MCP App dashboard:** sales, orders, stock and pending approvals shown inside Claude, with a link to the approval page
- Tested from Claude, with demo videos in the repo

`TypeScript` `MCP SDK` `Cloudflare Workers` `OAuth 2.1` `PostgreSQL` `Neon` `Vitest`

### Hala: bilingual AI booking receptionist (Arabic and English)

**An AI receptionist for salons, clinics and studios.** Customers chat with it on the business's website in Arabic or English: it answers only from the business's own FAQs and policies with sources, checks real availability, and books, moves or cancels appointments, each confirmed by the customer first. Staff can take over any conversation from an inbox.

🔗 **Live demo:** [hala-phi.vercel.app/demo](https://hala-phi.vercel.app/demo) · 💻 **Code:** [github.com/MostafaSaafan5517/hala](https://github.com/MostafaSaafan5517/hala) · 📖 **How it works:** [technical tour](https://github.com/MostafaSaafan5517/hala/blob/main/docs/how-it-works.md)

- **The AI never writes data itself:** it can only request actions through 8 validated server-side tools, and every booking is shown to the customer to confirm, with signed approvals that can't be tampered with
- **Double bookings are impossible, enforced by Postgres** (an exclusion constraint), proven by tests firing 20 simultaneous requests at one slot: exactly one succeeds
- **Grounded answers:** hybrid search (pgvector plus keywords) with Arabic-aware text handling; with nothing relevant found, it says it doesn't know and offers a person
- **Prompt injection can't change prices or rules,** tested with a model that deliberately obeys injected instructions
- **Cost control:** every AI call logged with tokens, cost and latency, with daily budgets (about $0.002 per reply)
- **482 database tests, 164 unit tests, 34 integration tests, 6 concurrency tests and 61 Playwright end-to-end tests,** plus an evaluation suite that scores the AI on 24 scripted conversations (the chosen model passed 24/24)

`Next.js` `TypeScript` `Supabase` `PostgreSQL` `pgvector` `Vercel AI SDK` `Playwright` `Vercel`

### Clubly: multi-tenant membership SaaS with Stripe Connect

**A membership platform for gyms, studios and clubs.**
Businesses connect Stripe, create membership plans, and members subscribe through Stripe Checkout, with a platform fee on every payment.

🔗 **Live:** [clubly-nine.vercel.app](https://clubly-nine.vercel.app) · 💻 **Code:** [github.com/MostafaSaafan5517/clubly](https://github.com/MostafaSaafan5517/clubly)

- Owner, admin and staff roles, each seeing only what their role allows, with expiring single-use team invites
- Stripe Connect onboarding, Stripe Checkout, the billing portal and payout dashboards
- Payments change only through **signed, idempotent webhooks**, with a **daily reconciliation job** that re-checks everything with Stripe
- Each business's data isolated with **row-level security**, and an **append-only change history** nobody can edit or delete
- **169 unit tests, 304 database tests and 76 Playwright end-to-end tests** (including real Stripe test payments), all running in CI
- **WCAG 2.1 AA** on all 74 screens in light and dark, after a full redesign with its own design system

`Next.js` `TypeScript` `Supabase` `PostgreSQL` `Stripe Connect` `Playwright` `Vercel`

### Sahra: interactive WebGL website scene that runs at 60 fps on phones

**The homepage of a fictional design studio, built around a living desert.** Up to 49,152 sand grains drift into dune lines on their own, scatter under the visitor's cursor or finger like a gust of wind, and change light through dawn, midday and dusk.

🔗 **Live:** [sahra-khaki.vercel.app](https://sahra-khaki.vercel.app) · 🧪 **The Lab:** [sahra-khaki.vercel.app/lab](https://sahra-khaki.vercel.app/lab/) · 💻 **Code:** [github.com/MostafaSaafan5517/sahra](https://github.com/MostafaSaafan5517/sahra)

- **All grain motion runs in a custom GLSL shader:** a noise flow field, dunes that creep downwind, sun shading and haze, with touch gusts passed to the GPU
- **Measured, not claimed:** 60 fps with all 49,152 grains on a mid-range Android phone (HONOR 400), and 60 fps on a 2015 laptop
- **Adaptive quality:** four quality tiers chosen per device, stepped down automatically by a live frame-rate monitor, pausing off screen and falling back to a still image where there's no GPU
- **Lighthouse 100 on mobile** in CI, zero layout shift, and WCAG AA contrast checked across every lighting state
- **The Lab:** a self-drawing Islamic geometric pattern in pure SVG and CSS, and a GSAP scroll story with pinned sections and a horizontal pan
- **One-line embed** for any website (Webflow, WordPress), loading the scene only where a GPU can run it
- **70 unit tests and 92 Playwright end-to-end tests,** with size budgets on every file

`Three.js` `WebGL` `GLSL` `TypeScript` `GSAP` `Vite` `Playwright` `Vercel`

### AI Lead Inbox: the same AI automation built in n8n and in Make.com

**Turns a busy inbox into sorted leads.** Emails and web form messages come in, AI sorts each one (hot lead, cold lead, support, spam) and pulls out the name, company, budget and need, then logs it and prepares a reply for a person to send.

💻 **Code:** [github.com/MostafaSaafan5517/lead-inbox-automation](https://github.com/MostafaSaafan5517/lead-inbox-automation) (MIT, with screenshots and setup steps)

- **Built twice:** self-hosted n8n (Docker) and Make.com, both live-tested end to end
- Gmail and web form intake, Google Sheets logging, Gmail labels and alerts for hot leads
- **Replies are saved as drafts, never sent automatically,** so a person always approves what goes out
- **Built to fail safely:** retries, a Dead Letter tab for anything that can't be processed, duplicate checks, and a prompt that ignores instructions hidden in messages
- **75 automated tests**

`n8n` `Make.com` `Gemini API` `Gmail` `Google Sheets` `Docker`

## 🛠️ Selected client work

Most of my client work lives in private repositories, so here is what I built and what it involved.

- **Operations platform for a hospitality group (14+ locations):** worked for about a year and a half on a large production system with 240+ REST endpoints. Led roughly 80% of the migration from the original system to its redesign, built the payments integration with idempotent webhook processing and reconciliation, and built an automated weekly sales report delivered to ownership and management.
- **My Permanent Lights, a lighting-control mobile app ([App Store](https://apps.apple.com/app/id6813178821) · [Google Play](https://play.google.com/store/apps/details?id=net.mypermanentlights.app)):** built a React Native (Expo, TypeScript) app shipped to both stores, covering EAS builds, TestFlight, an App Store review rejection and resubmission, and a follow-up release. LAN-first device control with cloud fallback and offline mode.
- **AI coaching platform for a relationship coach:** an attachment-style quiz with an AI chat and a personal AI healing plan, with a monthly AI spend cap, a daily message limit and a crisis check. It brought her 3 new clients in its first week and led to a larger paid phase: a paid program with Stripe packages, logins and progress saved across phone and computer.
- **Lynx ([collab-with-lynx.com](https://collab-with-lynx.com)):** a creator platform where I built authentication, onboarding and profiles on Supabase and PostgreSQL with row-level security.
- **Calimero ([calimeroshop.de](https://calimeroshop.de)):** a live restaurant ordering and POS system where I built the staff and admin tooling, the order flow and refund handling.

## 📚 Teaching

I also teach programming in Egypt: in-person courses in programming fundamentals and frontend development, including advanced JavaScript and React. Teaching keeps me sharp on the fundamentals and on explaining technical decisions clearly.

## 🧰 Languages and tools

<br>

<div align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=html,css,sass,js,ts,react,nextjs,tailwind,materialui,bootstrap,redux,nodejs,express,postgres,supabase,mongodb,githubactions,vercel,git,github,figma,postman,vscode&perline=12" />
  </a>
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/React%20Native-Expo-000020?style=flat-square&logo=expo&logoColor=white" alt="React Native with Expo">
  <img src="https://img.shields.io/badge/Stripe-Connect%20%26%20Billing-635bff?style=flat-square&logo=stripe&logoColor=white" alt="Stripe">
  <img src="https://img.shields.io/badge/Playwright-E2E%20testing-2ead33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright">
  <img src="https://img.shields.io/badge/Vitest-Unit%20testing-6e9f18?style=flat-square&logo=vitest&logoColor=white" alt="Vitest">
  <img src="https://img.shields.io/badge/pgTAP-Database%20testing-336791?style=flat-square&logo=postgresql&logoColor=white" alt="pgTAP">
  <img src="https://img.shields.io/badge/pgvector-RAG%20search-336791?style=flat-square&logo=postgresql&logoColor=white" alt="pgvector">
  <img src="https://img.shields.io/badge/Three.js-WebGL%20%26%20GLSL-000000?style=flat-square&logo=threedotjs&logoColor=white" alt="Three.js">
  <img src="https://img.shields.io/badge/GSAP-Animation-88CE02?style=flat-square&logo=greensock&logoColor=black" alt="GSAP">
  <img src="https://img.shields.io/badge/Vercel%20AI%20SDK-Tool%20calling-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel AI SDK">
  <img src="https://img.shields.io/badge/MCP-Servers%20%26%20Apps-000000?style=flat-square" alt="Model Context Protocol">
  <img src="https://img.shields.io/badge/Cloudflare-Workers-f38020?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare Workers">
  <img src="https://img.shields.io/badge/n8n-Automation-ea4b71?style=flat-square&logo=n8n&logoColor=white" alt="n8n">
  <img src="https://img.shields.io/badge/Make.com-Automation-6d00cc?style=flat-square&logo=make&logoColor=white" alt="Make.com">
</div>

<br>

## 🤝 Let's work together

I'm open to freelance and long-term remote work, and I can overlap with any U.S. or European time zone.
The best way to reach me is through [my Upwork profile](https://www.upwork.com/freelancers/~0104fa36ecdc4bf8a1).

<br>

<div align="center">
 <img width="1000" src="./assets/github-snake.svg" alt="snake"/>
</div>
