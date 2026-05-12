# Memo Paris — Brand Intelligence Dashboard

A live brand reputation and customer sentiment monitoring dashboard for **Memo Paris**, built as a single self-contained HTML file. Designed to be embedded in Notion via an iframe, or hosted on any static host (GitHub Pages, Netlify, Vercel).

## Features

- **5 monitoring tabs** — Brand CS Sentiment Health, Platforms, Alerts & Detection, Response Protocols, AI Layer
- **10 platforms tracked** — Trustpilot, Judge.me, Google, Instagram, TikTok, Facebook, Pinterest, Fragrantica, Reddit, X
- **12 markets** — interactive country filter + score sort (high→low / low→high)
- **Live clock** with pulse indicator
- **Animated chart** — 30-day weighted score trend (Chart.js)
- **Alert severity system** — Critical / Medium / Minor with cadence reference
- **Brand-safe response templates** — luxury tone, SLA guidance, escalation rules
- **AI situational analysis** — What happened / Why it matters / What to do next
- **Predictive risk scoring** — Reddit escalation likelihood, GEO/LLM authority risk

## Usage

### GitHub Pages (recommended for Notion embed)

1. Fork or clone this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your dashboard will be live at `https://yourusername.github.io/memo-paris-dashboard/`

### Notion embed

1. Copy your GitHub Pages URL
2. In Notion, type `/embed`
3. Paste the URL
4. Resize the block height to **700px+** for the full experience

### Local preview

Open `index.html` directly in any modern browser — no server or build step required.

## Structure

```
memo-paris-dashboard/
├── index.html      # Entire dashboard — HTML, CSS, JS in one file
└── README.md       # This file
```

## Dependencies (CDN — no install needed)

| Library | Version | Purpose |
|---|---|---|
| Chart.js | 4.4.1 | 30-day trend sparkline |
| Google Fonts | — | Cormorant Garamond · DM Mono · Outfit |

All dependencies load from CDN. The dashboard requires an internet connection to render fonts and the chart correctly.

## Data

All data is currently static and representative. To connect live data sources, replace the JS data arrays in `index.html` with API calls to:

- **Trustpilot** — Business API `/reviews/search`
- **Judge.me** — Shopify app API + webhook
- **Google Reviews** — Google My Business API
- **Reddit** — Official API (`/r/fragrance/search`)
- **Social signals** — Platform APIs (Meta, TikTok for Business, Pinterest API)

## Access

This dashboard is intended for internal use only. If hosting publicly, consider adding HTTP Basic Auth at the hosting layer (Netlify, Cloudflare Pages) to restrict access.

---

*Memo Paris — Brand Intelligence System · Confidential*
