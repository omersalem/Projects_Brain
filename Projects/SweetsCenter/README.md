# Project Overview

**SweetsCenter** (Almalaki Store / Luxury Bakery E-Commerce) is a mobile-first, high-performance e-commerce web application designed for a luxury bakery and sweets store with an embedded admin control panel, cash-on-delivery checkout flow, customer accounts, and order tracking.

The application features full RTL (Arabic) localization, visual branding, product management, category filtering, coupon systems, and automated Cloudflare R2 media storage pipelines.

# Repository

* **GitHub URL**: https://github.com/omersalem/SweetsCenter
* **Default Branch**: `main`
* **Visibility**: Private
* **Local Path**: `Unknown`
* **Last Updated on GitHub**: `2026-07-25`
* **Metrics**: Stars: 0 | Forks: 0 | Open Issues: 0

# Technologies

* **Languages**: TypeScript, SQL, HTML, CSS
* **Frameworks**: React 18, Vite, TailwindCSS, Radix UI (shadcn/ui), React Router v6, TanStack Query (React Query)
* **Database**: Supabase (PostgreSQL with Row Level Security & custom SQL procedures)
* **Infrastructure**: Cloudflare Workers (R2 upload worker & Telegram notification worker), Netlify Hosting
* **Cloud**: Supabase Cloud, Cloudflare (R2 Bucket Storage & Workers)
* **External Services**: EmailJS (email verification/resets), Telegram Bot API (order notifications)
* **Detected Stack**: React 18, TypeScript, Vite, TailwindCSS, Supabase, Cloudflare Workers & R2, Radix UI, TanStack Query, Lucide Icons

# Architecture

* **Frontend**: Mobile-first single page application (SPA) built with React 18, Vite, and TailwindCSS. Utilizes Radix UI primitives and Lucide icons for UI components.
* **Backend & Auth**: Supabase PostgreSQL database providing real-time data access, authentication, and SQL stored procedures for stock management and user role security.
* **Media & Assets**: Cloudflare R2 object storage coupled with Cloudflare Worker scripts (`r2-upload-worker.js`) for optimized asset uploads and low-cost CDN delivery.
* **Notifications**: Cloudflare Worker integration (`telegram-notify-worker.js`) triggering instant Telegram alerts on new customer orders.
* **Deployment**: Continuous integration and deployment via Netlify (`netlify.toml`) and Cloudflare Workers (`wrangler.r2-upload-worker.toml`).

# Current Status

Active production/development repository on `main` branch. Last updated July 25, 2026.

# Important Decisions

* **Cloudflare R2 for Storage**: Offloaded product image uploads to Cloudflare R2 via custom worker scripts (`r2-upload-worker.js`) to minimize Supabase egress costs.
* **Telegram Instant Order Alerts**: Integrated Telegram Webhook Workers for zero-latency admin order notifications.
* **Supabase RLS & Stored Procedures**: Implemented custom SQL migrations for admin password resets, stock checks, and row-level security.

# Known Issues

Open Issues Count: 0.

# Next Priorities

* Expand customer retention tools (favorites, loyalty coupons, repeat order history).
* Continuous optimization of R2 media pipeline and delivery caching.

# Notes

Synchronized and updated via `github-project-sync` skill on 2026-07-26.

---

## Knowledge Graph & System Links

* **Global Knowledge**: [[AGENTS]] | [[RULES]] | [[Engineering Principles]] | [[Lessons Learned]]
* **Project Skills**: [[Skills/feature/SKILL]] | [[Skills/fix/SKILL]] | [[Skills/review/SKILL]] | [[Skills/new/SKILL]]
