# SEO Watch — eastlakeview503.relahq.com

Two-tier automated SEO monitoring for the **Riva Condominium #503** listing microsite
(`https://eastlakeview503.relahq.com/`, Rela property ID 257763116, 1550 Eastlake Ave E,
Seattle WA 98102, $649,888, MLS# 2556157, built 1997).

## Agents

| Tier | Model | When | Job |
|---|---|---|---|
| **1 — Weekly SEO Watch** | Sonnet | Mon 08:00 UTC | Fetch the live page, detect regressions vs baseline, detect pending Rela fixes landing, track index/rank, benchmark competitors. Commits `reports/YYYY-MM-DD.md`, then triggers Tier 2. |
| **2 — SEO Strategist** | Opus | triggered by Tier 1 (+ Mon 09:00 UTC safety net) | Review what changed on the live site (Keep/Fix/Revert/Escalate), produce the week's action package, competitor deep-dive. Commits `reports/YYYY-MM-DD-strategy.md`, updates `ACTION-QUEUE.md`, sends the consolidated alert. |

Neither agent can edit Rela or Google Search Console (cloud, no browser/login). They detect,
analyse, and write executable specs into `ACTION-QUEUE.md` for a browser session to run.

## Layout

- `reports/YYYY-MM-DD.md` — Tier 1 weekly watch
- `reports/YYYY-MM-DD-strategy.md` — Tier 2 strategy + review
- `state/last-snapshot.json` — last observed state, for week-over-week diffs
- `state/competitors.json` — tracked competitor set + first-seen dates
- `ACTION-QUEUE.md` — live to-do for browser sessions (top = do now)

## Baseline (set 2026-09-10, via Chrome, in the Rela editor)

- `<title>` = `Riva Condos #503, 1550 Eastlake Ave E – Seattle Condo for Sale`
- meta description contains `Riva Condominium` + `MLS# 2556157`
- og:title contains `Riva Condos #503`
- JSON-LD: `yearBuilt` 1997, `offers.price` 649888, name = clean address, description starts
  `Top-floor 2-bed, 2-bath condo for sale at Riva Condominium`
- body contains `Riva Condominium` and `Riva Condos`

## Pending Rela-platform fixes (all still absent as of 2026-09-10 — submitted via Rela chat)

`twitter:card`, `og:url`, `og:locale`, fixed `twitter:image:alt`, H1 =
`1550 Eastlake Ave E #503, Seattle, WA 98102`, JSON-LD `numberOfBedrooms` /
`amenityFeature` / `petsAllowed` / `containedInPlace`, `<img loading="lazy">`,
`/sitemap.xml` = 200, `robots.txt` without `Crawl-delay: 10` + with a `Sitemap:` line,
`/llms.txt` populated.
