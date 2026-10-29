# Team Sponsorship Directory

A public Zoomph reference of team jersey and helmet sponsors (NBA, G League, WNBA, NHL, MLS and NWSL jersey sponsors, and NHL helmet decals), past, present and announced, with links to the reporting behind them. Live at https://directory.zoomphstats.com/. Owner: Andrew Ciampini (Data Quality and Operations, Benchmarking).

**Public by Nick Cronin's decision (2026-10-23).** Everything in `public/` is readable by anyone, so `public/deals.json` must only ever be the public export: the fields the page shows, with no research notes and no internal bookkeeping.

## What's in this repo

| Path | What it is |
|---|---|
| `public/index.html` | The whole site: one static page, no build step. |
| `public/deals.json` | The data (public export): every directory entry's public fields, plus the date it was exported and the last news-check date. |
| `vercel.json` | Vercel settings: serve `public/`, no framework, and `noindex` headers so search engines skip it. |

There are no dependencies, no build command, no environment variables and no secrets.

## How the data is kept up to date

The master copy of the directory, with full research notes, lives on claude.ai. A daily news check proposes new sponsorship announcements there, and Andrew approves or rejects each one. After approving, Andrew re-exports the public data and replaces `public/deals.json` here. Each commit to `main` redeploys the site, so the site can trail the master copy by a day or two. The "Data as of" date at the top of the page shows when it was last updated.

Don't edit `public/deals.json` by hand. Changes go through the master copy so they get reviewed.

## Vercel settings

| Setting | Value |
|---|---|
| Framework preset | Other |
| Root directory | `./` (repo root) |
| Build command | none |
| Output directory | `public` (also set in `vercel.json`) |
| Install command | none |
| Environment variables | none |
| Deployment Protection | Off: the site is public by decision (2026-10-23) |

## Basis

Every entry comes from public announcements and press coverage: teams, leagues, sponsors and news outlets. Reported deal values and terms are the cited outlet's figures, not Zoomph valuations. Confidence (High / Medium / Low) is explained on the page's "How it works" tab.
