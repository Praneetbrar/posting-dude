# Posting Dude

**Manual content marketing and distribution for indie products that ship.**

Live site: **[postingdude.com](https://postingdude.com)**

![Posting Dude logo](https://postingdude.com/logo.png)

---

## What Posting Dude is

Posting Dude is a **done-for-you distribution partner** for indie founders. You focus on building; we **research, write, format, and publish** AEO- and SEO-friendly content about your product across **launch platforms, directories, and social**—so you don’t disappear after launch day.

It’s **not** a self-serve scheduler: work is **manual and quality-capped** (project limits per plan), built for founders who want consistent visibility without turning marketing into a second job.

---

## Why it exists

- **Shipping is easier than being found.** A launch spike often fades; without ongoing presence, products vanish from feeds and search.
- **SEO and AI discovery need a real footprint.** One blog post rarely moves the needle; you need clear explanations in **trusted places** so humans—and AI answers—can reference you.
- **Distribution is time-consuming.** Research, writing, formatting, and cross-posting across many sites is work most small teams don’t have bandwidth for.

Posting Dude exists to **own that distribution layer** for you, every month.

---

## Benefits

| Benefit | What it means for you |
|--------|------------------------|
| **Consistent presence** | Ongoing publishing—not a one-off launch post. |
| **Multi-channel footprint** | Articles and posts where indie builders and early adopters actually look. |
| **Clear positioning** | Content that explains what you built, for search and AI-friendly discovery. |
| **Time back** | No juggling six tabs and copy-paste workflows; we execute the distribution. |
| **Simple plans** | **Launch** for one product; **Studio** when you’re running multiple bets. |

---

## Features

### Distribution & content

- **Monthly articles** on **Aura++**, **IndieHunt**, **EarlyHunt**, and **Uno Directory** (per plan and project count).
- **Studio** adds **X** and **LinkedIn** posts **per project** each month.
- Content is tuned for **discoverability** (SEO/AEO-style clarity, not generic fluff).

### Customer experience (product)

- **Sign in** (e.g. Google) and **guided onboarding** to capture goals, product details, and plan choice.
- **Dashboard**: overview, project switcher, **billing** (Polar), **settings**, and **reports** where published links show up.
- **Suggest edits** from the dashboard so users can request changes; operators can manage fulfillment from an **admin** area (restricted access).

### Plans & limits

- **Launch**: **1 project**; directory articles across the four platforms for that project.
- **Studio**: **up to 3 projects**; full directory coverage **plus** X and LinkedIn per project, plus **priority support**.

*(Exact entitlements match the live pricing UI in [`src/components/pricing.tsx`](src/components/pricing.tsx).)*

---

## Pricing

Simple **monthly** pricing (also reflected on the site):

| Plan | Price | Best for |
|------|-------|----------|
| **Launch** | **$59/mo** | One product; one month of focused distribution across Aura++, IndieHunt, EarlyHunt, Uno. |
| **Studio** | **$99/mo** | Up to **3** products; full monthly distribution including **X + LinkedIn** per project + priority support. |

See **[postingdude.com/pricing](https://postingdude.com/pricing)** for the full feature lists and CTAs.

---

## Where we publish

We distribute to channels where indie and early-adopter audiences discover tools:

- [Aura++](https://auraplusplus.com)
- [IndieHunt](https://indiehunt.io)
- [EarlyHunt](https://earlyhunt.com)
- [Uno Directory](https://uno.directory)
- **X** and **LinkedIn** (Studio; per project)

Details: **[postingdude.com/platforms](https://postingdude.com/platforms)**  
Story & positioning: **[postingdude.com/why](https://postingdude.com/why)**

---

## How it works (customer journey)

1. **Share your projects** — What you’re building, positioning, and which links matter.
2. **We write & optimise** — Drafts that explain the product clearly for search and discovery.
3. **We post everywhere** — Publishing across the platforms in your plan; you track **reports** in the dashboard.

---

## Screenshots & marketing assets

![Open Graph preview](https://postingdude.com/og.png)

| Asset | Purpose |
|-------|---------|
| [https://postingdude.com/logo.png](https://postingdude.com/logo.png) | Logo (navbar, emails, README). |
| [https://postingdude.com/og.png](https://postingdude.com/og.png) | **Open Graph / Twitter** card image for link previews. |

**Tip:** For landing pages, pitch decks, or App Store–style shots, capture the **homepage hero** (https://postingdude.com), **pricing** (https://postingdude.com/pricing), and **dashboard reports** after login. Store extras under `docs` or `.github` if you want them versioned without bloating the repo.

---

## Tech stack (this repository)

- **Next.js** (App Router), **React**, **TypeScript**
- **Tailwind CSS** + UI primitives (Radix-style components)
- **NextAuth** (Google OAuth), **Postgres** (e.g. Neon) via `postgres`
- **Polar** for subscriptions / checkout
- **Resend** for transactional email

---

## Local development

### Prerequisites

- **Node.js** 18+ (20+ recommended)
- **pnpm**

### Install & run

```bash
pnpm install
cp .env.example .env
# Fill in DATABASE_URL, NEXTAUTH_*, Google OAuth, Resend, etc.
pnpm dev
```

Open **http://localhost:3000**.

Production also needs Polar, site URL, and related secrets—mirror what you use on your host (e.g. Vercel). See `.env.example` for the base set; extend as needed for billing webhooks and product IDs.

---

## Project layout (high level)

- `src/app/(home)/` — Marketing homepage
- `src/app/pricing/`, `src/app/platforms/`, `src/app/why/` — Marketing pages
- `src/app/dashboard/` — Authenticated customer dashboard
- `src/app/admin/` — Operator admin (protect with `ADMIN_EMAIL` in production)
- `src/components/pricing.tsx` — Plan definitions and pricing UI
- `public/` — Static assets (`logo.png`, `og.png`, manifests, etc.)

---

## Contact

For business questions about Posting Dude, use the contact options on **[postingdude.com](https://postingdude.com)**.
