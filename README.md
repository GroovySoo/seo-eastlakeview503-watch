# SEO Watch — eastlakeview503.relahq.com

Three-tier automated SEO monitoring and implementation for the **Riva Condominium #503** listing
microsite (`https://eastlakeview503.relahq.com/`, Rela property ID 257763116, 1550 Eastlake Ave E,
Seattle WA 98102, $649,888, MLS# 2556157, built 1997).

## Agents

| Tier | Runs where | When | Job |
|---|---|---|---|
| **1 — Evidence gatherer** | Cloud routine (Sonnet) | Mon 08:00 UTC | Fetch the live page, check indexability, run tracked SERP queries, benchmark competitors, verify open action items. Writes `reports/EVIDENCE-<date>.md` + `state/observations-<date>.json`. Records facts only — never recommendations. |
| **2 — Strategist** | Cloud routine (Opus) | Mon 10:00 UTC | Diff observations against the baseline, decide what matters, write `reports/STRATEGY-<date>.md`, rewrite `ACTION-QUEUE.md`, update the baseline, post the memo to Slack `#all-seo-eastlake`. |
| **3 — Implementer** | Local scheduled task on the owner's PC, driving Chrome | Mon 11:05 local | Take `## Do now` from `ACTION-QUEUE.md`, carry the doable items out in the owner's logged-in Chrome (Rela editor, Search Console, Analytics), stop for **one batched approval** before anything is saved, verify each change live, write `reports/IMPLEMENTATION-<date>.md`, post a summary to Slack. |

The tiers are independent scheduled jobs; the gaps between them are the coupling. Tier 2 handles a
missing or failed Tier 1 run explicitly (see the gate below); Tier 3 stops if there is no recent
STRATEGY file.

Tiers 1 and 2 run in the cloud with no browser and no logins. Tier 3 is the only tier that can change
anything live, and only because it runs on the owner's own machine with their existing sessions. It
never types passwords, creates accounts, or posts publicly as the owner — those go back to the owner
as plain-language steps in the implementation report.

### Why Tier 3 doesn't mark its own work done

Tier 3 writes only `reports/IMPLEMENTATION-*.md`. It never edits `ACTION-QUEUE.md`. An item leaves the
queue only when **Tier 1 observes the change on the live page** the following week and Tier 2 closes it.
The agent that made a change is never the one that certifies it worked.

## The evidence contract

Tier 1 writes a header block at the top of every evidence report. Tier 2 reads it **first** and
uses it to decide whether the run is trustworthy:

```
---
run_date: <YYYY-MM-DD>
status: complete | partial | failed
fields_captured: <N>/<M>
fetch_failures: <sources that failed after browser-UA retry, or "none">
listing_status: active | price_changed | pending | sold | unknown
indexed: yes | no | unknown
---
```

**Why this exists:** on 2026-09-11 a Tier 1 run hit a total network block and produced an evidence
file that was structurally well-formed but almost entirely empty. Without a status field, Tier 2
would have read it as valid and overwritten the baseline with nulls — silently destroying the
week-over-week history the whole system exists to produce.

The gate Tier 2 applies:

| status | Tier 2 behaviour |
|---|---|
| `complete` | Normal run. Overwrite the baseline. |
| `partial` | Update only fields that are non-null in the observations JSON. Report which fields went stale. |
| `failed` / file missing | **Do not touch the baseline.** Write the memo, flag the monitoring gap, still post to Slack. |

## Ownership rules

- Only **Tier 1** writes `reports/EVIDENCE-*.md` and `state/observations-*.json`.
- Only **Tier 2** writes `reports/STRATEGY-*.md`, `ACTION-QUEUE.md`, and `state/last-snapshot.json`.
- Only **Tier 3** writes `reports/IMPLEMENTATION-*.md`, and it writes nothing else.
- Tier 1 must never touch `last-snapshot.json` — an agent that writes its own baseline can drift
  against itself without ever detecting a change.
- All tiers push directly to `main`. None creates branches or pull requests.

## Layout

- `reports/EVIDENCE-<date>.md` — Tier 1 raw facts (human-readable)
- `state/observations-<date>.json` — Tier 1 same facts, machine-readable, for mechanical diffing
- `reports/STRATEGY-<date>.md` — Tier 2 decisions and the week's action package
- `state/last-snapshot.json` — the baseline; only Tier 2 writes it
- `state/competitors.json` — tracked queries, competitor set with URLs, and fetch hints
- `ACTION-QUEUE.md` — live to-do for browser sessions (top = do now)

## Known environment facts

These are recorded in `state/competitors.json → fetch_hints` and in both agent prompts so they are
never rediscovered at runtime:

- The target and several competitors return **403 from CloudFront/Cloudflare to default curl/tool
  user-agents**. A browser User-Agent is required. A default-UA 403 is expected, not a finding.
- `WebFetch` returns **405** against the target domain. Use curl.
- `www.rsir.com` is behind a **Cloudflare JS challenge** and is not fetchable by curl with any UA.
  Marked `fetchable: false`. Do not retry it.
- `pagespeed.web.dev` is a JS shell that returns no data to a fetcher. Use the PageSpeed REST API,
  one attempt; a 429 means the public quota is exhausted.
- The page has **two JSON-LD blocks**. The second is injected client-side by an IIFE and must be
  extracted by regex on `l.text` — parsing `<script>` tags alone misses it.

## Baseline (set 2026-09-10, via Chrome, in the Rela editor)

- `<title>` = `Riva Condos #503, 1550 Eastlake Ave E – Seattle Condo for Sale`
- meta description contains `Riva Condominium` + `MLS# 2556157`
- og:title contains `Riva Condos #503`
- JSON-LD: `yearBuilt` 1997, `offers.price` 649888, name = clean address, description starts
  `Top-floor 2-bed, 2-bath condo for sale at Riva Condominium`
- body contains `Riva Condominium` and `Riva Condos`

## Pending Rela-platform fixes (submitted via Rela chat, still absent as of 2026-09-11)

`twitter:card`, `og:url`, `og:locale`, fixed `twitter:image:alt`, H1 =
`1550 Eastlake Ave E #503, Seattle, WA 98102`, JSON-LD `numberOfBedrooms` /
`amenityFeature` / `petsAllowed` / `containedInPlace`, `<img loading="lazy">`,
`/sitemap.xml` = 200, `robots.txt` without `Crawl-delay: 10` + with a `Sitemap:` line,
`/llms.txt` populated.

## Lifecycle

This monitors a **single listing**, which will eventually go under contract and sell. Tier 1
records `listing_status` every run. When it reports `pending` or `sold`, Tier 2 says so at the top
of the memo and recommends winding the routines down at https://claude.ai/code/routines. The
system is designed to end, not to run forever.
