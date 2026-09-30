# Mineral Link Web

Frontend for Mineral Link — a platform that connects Uganda's small-scale and artisanal miners directly with verified buyers and exporters, and gives miners access to fair, transparent pricing for minerals like gold, tin, and tungsten.

## The Problem

Small-scale miners often sell through middlemen who decide what price information reaches them, so miners are frequently underpaid for their minerals. Mineral Link solves this by giving miners a direct line to verified buyers and clear, current pricing, instead of relying on what a middleman chooses to tell them.

## Who It Is For

- **Miners** — see current mineral prices and list what they have for sale.
- **Buyers / Exporters** — browse verified miners and listings and make direct contact.
- **Admins** — verify accounts, manage listings, and keep the platform trustworthy.

## Tech Stack and Why

| Tool | Why it was chosen |
|---|---|
| **Next.js** | A React framework that handles routing, server-side rendering, and page structure out of the box. This matters for Mineral Link because pricing pages need to load fast and be easy to find (good for search visibility), and Next.js supports that without extra setup. |
| **TypeScript** | Same reasoning as the API — catching data-shape mistakes (e.g. treating a price as text instead of a number) before they become bugs, and making the codebase easier for a mentor or future teammate to read. |
| **React** (via Next.js) | Component-based UI, which fits Mineral Link well since the same pieces (a price card, a listing card, a user profile) repeat across miner, buyer, and admin views. |

This is a documentation-only step, so no packages are installed yet. The stack above is the plan for when coding starts.

## How to Install and Run Locally

> Note: at this stage, this repository only contains documentation. These are the steps that will apply once the actual frontend code is added.

1. **Install Node.js** (LTS version) from [nodejs.org](https://nodejs.org).
2. **Clone this repository:**
   ```bash
   git clone <repository-url>
   cd mineral-link-web
   ```
3. **Install dependencies** (once `package.json` exists):
   ```bash
   npm install
   ```
4. **Set up environment variables:**
   - Copy `.env.example` to `.env.local`
   - Set `NEXT_PUBLIC_API_URL` to point at the running API (e.g. `http://localhost:4000`)
5. **Run the development server:**
   ```bash
   npm run dev
   ```
6. Open `http://localhost:3000` in a browser.

## Folder Structure (Planned)

```
mineral-link-web/
├── app/
│   ├── (miner)/             # Pages and layout specific to the miner role
│   ├── (buyer)/              # Pages and layout specific to the buyer role
│   ├── (admin)/               # Pages and layout specific to the admin role
│   ├── components/             # Reusable UI pieces (price card, listing card, nav bar)
│   ├── lib/                     # Helper functions, e.g. functions that call the API
│   └── layout.tsx                # Root layout shared by all pages
├── public/                  # Static files (images, icons)
├── .gitignore                 # Files/folders Git should not track (node_modules, .next, .env, etc.)
├── LICENSE                     # MIT License
├── package.json                 # Project dependencies and scripts (to be added when coding starts)
└── README.md                     # This file
```

## Related Repository

The backend API lives in a separate repository: `mineral-link-api`.

## Status

Documentation phase. No application code has been written yet — this is intentional, per the current task. Code will begin after mentor review.
