# LeadForge Local

A zero-API-key, local-first B2B map lead finder and cold outreach utility built for agencies, freelancers, and web developers targeting local businesses.

## Key Features

- **Interactive Dark-Mode Radius Map** — Pinpoint any location, drag or resize the search radius in kilometers, and inspect color-coded lead markers across the target area.
- **Photon + OSM Batch Hydration** — Queries Komoot Photon and `nw`-scoped OpenStreetMap Overpass in parallel with bounded Nominatim fallback and OSM v0.6 batch tag hydration (`nodes.json` / `ways.json`) for fast, resilient discovery.
- **No-Website Prioritization** — Automatically classifies and ranks leads into `NO_WEBSITE` (Hot Lead), `SOCIAL_ONLY` (Needs Site), and `HAS_WEBSITE` tiers, with instant filtering and unreachable-lead cleanup.
- **Automated Website Email Scraping** — Multi-threaded scraper checks `HAS_WEBSITE` homepages and internal contact/about pages while skipping `NO_WEBSITE` and `SOCIAL_ONLY` leads for speed.
- **DuckDuckGo Contact Discovery** — Free web-search enrichment discovers public emails, phone numbers, and Facebook/Instagram pages for businesses without a website.
- **Gmail SMTP Sender with Live Diagnostics** — Sends personalized outreach via `smtp.gmail.com` (SSL port `465` with automatic STARTTLS port `587` fallback), includes a `TEST LOGIN` pre-flight check, configurable anti-spam delays, conditional `{{#no_website}}` template blocks, and an inline status log.
- **Guided WhatsApp Fallback Queue** — Normalizes local and international phone numbers, generates pre-filled `wa.me` outreach links, and steps sequentially through phone-only leads with `WA SENT` tracking.

## Tech Stack

- **Backend:** `Python`, `Flask`, `SMTP`
- **Frontend:** `Leaflet.js`, `CartoDB Dark Matter`, `Tailwind CSS`

## Preview

![Dashboard](screenshots/dashboard.png)

> Source code is kept private.
