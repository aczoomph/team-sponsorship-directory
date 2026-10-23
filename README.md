# Team Sponsorship Directory

An internal Zoomph reference of team jersey and helmet sponsors (NBA, G League, NHL jersey patches and NHL helmet decals), past, present and announced, with sources for every entry. Owner: Andrew Ciampini (Data Quality and Operations, Benchmarking).

**Internal only.** The site must sit behind Vercel Deployment Protection covering all deployments, including the production domain. No anonymous access.

## What's in this repo

| Path | What it is |
|---|---|
| `public/index.html` | The whole site: one static page, no build step. |
| `public/deals.json` | The data: every directory entry, plus the date it was exported and the last news-check date. |
| `vercel.json` | Vercel settings: serve `public/`, no framework, and `noindex` headers so search engines skip it. |

There are no dependencies, no build command, no environment variables and no secrets.

## How the data is kept up to date

The master copy of the directory lives on claude.ai, where a daily news check proposes new sponsorship announcements and Andrew approves or rejects each one. After approving, Andrew re-exports the data and replaces `public/deals.json` here. Each commit to `main` redeploys the site, so the site can trail the master copy by a day or two. The "Data as of" date at the top of the page shows when it was last updated.

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
| Deployment Protection | Vercel Authentication, scope **All Deployments** (Standard Protection leaves the production domain public) |

## Basis

Every entry comes from public announcements and press coverage. Reported deal values and terms are the cited outlet's figures, not Zoomph valuations. Confidence (High / Medium / Low) is explained on the page's "How it works" tab.
