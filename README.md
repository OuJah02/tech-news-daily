# ⚡ Daily Tech Pulse

A single-page tech news dashboard. Every day it pulls the latest stories from ten major technology publications, filters out anything that isn't tech, and lays them out as a dense mosaic of clickable article cards — sized by how much each story has to say.

**Live site:** https://oujah02.github.io/tech-news-daily/

## Features

- **Tech-only, day-by-day** — shows today's technology stories (new products, emerging tech, R&D, industry news) and automatically rolls over at midnight. Use the ◀ ▶ arrows to look back at previous days (up to 10 days are remembered as you use it).
- **Ten sources** — The Verge, Ars Technica, TechCrunch, Engadget, Wired, MIT Technology Review, ZDNet, IEEE Spectrum, New Atlas, and Gizmodo. Filter to specific outlets with the chips under the header.
- **Smart mosaic layout** — meaty stories get big feature tiles with large images; quick blurbs get compact text tiles. Small tiles backfill the gaps so the page fills with minimal scrolling.
- **Non-tech filter** — entertainment, sports, celebrity, and shopping-deal stories that sneak into tech feeds are dropped unless they have a genuine tech angle.
- **Summaries with links** — each card shows the publication's own summary; click any card to read the full article at the source.

## How it works

Everything lives in one file, `index.html` — no build step, no backend, no dependencies. The page fetches each publication's RSS/Atom feed in the browser (via [rss2json](https://rss2json.com) with public CORS proxies as fallback), parses and de-duplicates the stories, and caches them in `localStorage` so past days stay browsable.

## Usage

Just open the live site and bookmark it (**Ctrl+D**). For an app-style shortcut with its own window: Chrome menu → **Cast, save and share → Create shortcut**.

It also works fully offline-hosted — download `index.html` and double-click it.
