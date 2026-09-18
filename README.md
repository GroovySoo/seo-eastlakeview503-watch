# SEO Watch — eastlakeview503.relahq.com

Three-tier automated SEO monitoring and implementation for the **Riva Condominium #503** listing
microsite (`https://eastlakeview503.relahq.com/`, Rela property ID 257763116, 1550 Eastlake Ave E,
Seattle WA 98102, $649,888, MLS# 2556157, built 1997).

## Agents

| Tier | Runs where | When | Job |
|---|---|---|---|
| **1 — Evidence gatherer** | Cloud routine (Sonnet) | Mon 08:00 UTC | Fetch the live page, check indexability, run tracked SERP queries, benchmark competitors, verify open action items. Writes `reports/EVIDENCE-<date>.md` + `state/observations-<date>.json`. Records facts only — never recommendations. |
| **2 — Strategist** | Cloud routine (Opus) | Mon 10:00 UTC | Diff observations against the baseline, decide what matters, write `reports/STRATEGY-<date>.md`, rewrite `ACTION-QUEUE.md`, update the baseline, post the memo to Slack `#all-seo-eastlake`. |
| **3 — Implementer** | Cloud routine (Opus), headless Playwright inside the sandbox | Mon 11:05 UTC | Take `## Do now` from `ACTION-QUEUE.md`; **auto-apply** only allowlisted additive Custom-Script JSON-LD edits (verified before/after), **draft everything else** (Property Description, SEO & Social, Details, Theme & Contacts, Photo Gallery, ...) into the report for the owner to apply by hand; write `reports/IMPLEMENTATION-<date>.md`, post a summary to Slack. Can also still be run interactively/locally (via the `playwright` MCP browser) for anything outside the allowlist. |

The tiers are independent scheduled jobs; the gaps between them are the coupling. Tier 2 handles a
missing or failed Tier 1 run explicitly (see the gate below); Tier 3 stops if there is no recent
STRATEGY file.

> **Audit pass, 2026-09-18.** A senior-SEO review of the loop itself is in
> [`reports/AUDIT-2026-09-18.md`](reports/AUDIT-2026-09-18.md). Verdict: the machinery is sound, the
> strategy had a hole — the #1 lever (inbound links) was asserted every week and never measured, and
> the two link placements being prescribed (email signature, LinkedIn Featured) carry no SEO value
> at all. `state/competitors.json` and `ACTION-QUEUE.md` were corrected in that pass, and the three
> prompt patches in §3 of that report have since been **applied to all three trigger prompts**
> (Tier 1 `trig_01QMErY82dD2WJk2D3TBK1MZ`, Tier 2 `trig_01NZnayoAnxJub2cxbbbncPz`, Tier 3
> `trig_01CBSS7zrhSfhEq4L6mCbHCF`) via `RemoteTrigger`, in effect starting the next fire of each.
> Still open, and still the owner's call (§5 of the audit): make the repo private (§1.5 — it
> currently outranks the listing for its own brand token and carries the owner's phone/email in
> plaintext), settle the `Senghor`/`Senghore` spelling (§1.6), paste `RELA_STORAGE_STATE_JSON` into
> the Tier 3 routine (or decide to retire that routine per §4.1 once `containedInPlace` ships), and
> the monthly GSC → Links reading.

Tiers 1 and 2 run in the cloud with no browser and no logins. Tier 3 is the only tier that can change
anything live, and only because it runs against a logged-in browser session on the owner's own
machine. It never types passwords, creates accounts, or posts publicly as the owner — those go back
to the owner as plain-language steps in the implementation report.

### How Tier 3 gets a logged-in browser (changed 2026-09-18, twice)

Tier 3 used to drive the owner's real Chrome via the Claude-in-Chrome extension, which reused
whatever the owner was already logged into. That broke on 2026-09-16: the extension refused
navigation to relahq.com/rela.com ("Navigation to this domain is not allowed") for reasons unrelated
to login — a site-permission setting in the extension itself. The first fix (same day) was to switch
the *local* Tier 3 to the `playwright` MCP browser, which runs with a persistent Chrome profile
(`~/.claude.json` → `mcpServers.playwright`, `--user-data-dir C:\Users\<owner>\.playwright-mcp-profile`)
that keeps a login across runs on that one machine.

**The owner then asked for Tier 3 to run fully in the cloud, like Tier 1/2 — not local.** That's a
different mechanism, documented here.

Tier 3 is now also a cloud routine: **`SEO Watch — Tier 3 implementer (eastlakeview503)`**
(trigger id `trig_01CBSS7zrhSfhEq4L6mCbHCF`, model Opus, cron `5 11 * * 1` UTC — an hour after Tier 2,
same shared environment `env_014LSLvRuau5UepuZeL1vEkt`). It runs a headless Chromium
(Playwright, installed at the start of each run) inside that cloud sandbox, not a browser on the
owner's PC.

**Two hard constraints shaped this design:**

1. **No agent can extract or relay the Rela session cookie itself.** Claude Code's own permission
   system blocks "credential materialization" — reading a live session's cookies into an agent's
   context — even when the owner explicitly approves it. So the owner must paste the session into the
   cloud routine's config themselves; no agent (local or cloud) ever sees the value in transit.
2. **Rela's save flow is a token-gated Drupal 7 AJAX form**, not a simple API: every save needs a
   fresh `form_build_id`/`form_token` scraped from the edit page's own HTML, plus ~80 supporting
   fields a real browser generates automatically. A hand-written `curl` replay would be brittle and
   silently break on any Rela front-end change. So Tier 3 runs an actual (headless) browser inside
   the cloud sandbox rather than replaying raw HTTP requests.

**Because a scheduled cloud run has no one present to approve anything mid-run**, Tier 3's prompt
carries a hard-coded allowlist instead of the old "one batched approval" pause: it may only
**auto-save** additive edits to the Advanced → Custom Script JSON-LD (the `ApartmentComplex` /
`RealEstateAgent` pattern already live, using facts already recorded in this repo), always
JSON-validated before and after. Everything else it drafts into `reports/IMPLEMENTATION-<date>.md`
as a proposed change for the owner to apply by hand — it never touches Property Description, SEO &
Social, Details, Theme & Contacts, Photo Gallery, or anything else live. See the routine's own prompt
(`https://claude.ai/code/routines` → that routine → its prompt) for the exact rules; they're
authoritative over this summary if the two ever disagree.

**Outstanding — the owner still needs to do this once:** the routine reads its Rela session from the
environment variable `RELA_STORAGE_STATE_JSON`. The `RemoteTrigger` API explicitly refused to accept
`environment_variables` on a trigger ("not supported on triggers — trigger configs are persisted and
replayed on every fire"), so this can't be set via the API/agent at all — it has to be set through the
claude.ai UI for this routine (`https://claude.ai/code/routines` → **SEO Watch — Tier 3 implementer
(eastlakeview503)** → look for an environment variables / secrets section). Paste the **entire
contents** of the local file `.auth/rela-storage-state.json` (produced by the one-time interactive
login below) as the value. Until that's done, Tier 3's cloud runs will detect the missing credential,
skip all Rela edits, and say so in the report and Slack message — a safe no-op, not a silent failure.

**Local one-time login (still needed, to produce/refresh the file above):** open an interactive
Claude Code session, navigate the `playwright` browser to `https://www.relahq.com/user/login`, log in
by hand, then export the session with Playwright's `context.storageState()` to
`.auth/rela-storage-state.json` (**gitignored, never committed** — it's equivalent to the account
password). First done 2026-09-18; the Rela auth cookie (`SESS…`/`SSESS…`, Drupal session) expires
**2026-10-11**. When it expires, repeat this login, re-export the file, and re-paste it into the cloud
routine's `RELA_STORAGE_STATE_JSON` — roughly monthly. The local `playwright` MCP profile also still
carries the login for anyone running Tier 3 interactively instead of via the cloud routine.

### Why Tier 3 doesn't mark its own work done

Tier 3 writes only `reports/IMPLEMENTATION-*.md`. It never edits `ACTION-QUEUE.md`. An item leaves the
queue only when **Tier 1 observes the change on the live page** the following week and Tier 2 closes it.
The agent that made a change is never the one that certifies it worked.

#### …and the exception that rule needs (added 2026-09-18)

Some facts Tier 3 learns can **never** appear on the live page, so under the rule as originally
written they were simply lost. Three of them sat in `ACTION-QUEUE.md` as open items for up to two
weeks after they had been settled:

| Fact | Learned | Still shown as open until |
|---|---|---|
| Search Console: "URL is on Google", Indexed = 1, Not indexed = 0 | 2026-09-16 | 2026-09-18 |
| Rela's photo editor has **no alt-text field at all** | 2026-09-18 | 2026-09-18 |
| Owner supplied phone / brokerage / bio URL | 2026-09-16 | 2026-09-18 |

So: **Tier 2 reads every `reports/IMPLEMENTATION-*.md` newer than its own last run** and folds those
findings into the queue and, where they are settled state, into the baseline. Tier 3 ends each report
with a `## Facts for Tier 2` section listing exactly those unobservable facts. Tier 3 still never
writes `ACTION-QUEUE.md`, and a change to the live page is still certified only by Tier 1 — what
crosses the gap is out-of-band knowledge, not self-certified work. (Prompt patches: see
`reports/AUDIT-2026-09-18.md` §3.)

### Measuring the #1 lever

The system's whole thesis is that inbound links are the only thing that will move this page. Until
2026-09-18 that number was hard-coded at scaffold time and copied forward every week — asserted,
never measured. Two mechanisms now measure it:

1. **Automated, weekly (Tier 1):** `state/competitors.json → mention_query` — a literal search for
   `"eastlakeview503.relahq.com"`, with this repo excluded as a known self-mention. Any other domain
   that appears is a real new inbound mention and is the headline of that week's memo.
2. **Authoritative, monthly (owner):** Search Console → **Links** → "Top linking sites". Under a
   minute, and the only source that reflects what Google actually counts.

`state/competitors.json → link_targets` carries five **named, verified-live** targets ranked by
realistic value, so the weekly ask is specific rather than generic. It also records what does **not**
count: an email signature is not a page on the web and is never crawled, and LinkedIn "Featured"
links are nofollow and client-rendered. Neither may be counted toward the link goal.

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
- **PageSpeed is switched off** (`competitors.json → fetch_hints.pagespeed_skip: true`, 2026-09-18).
  Three consecutive runs returned 429 against a public quota of 0/day, so no data will ever come
  back without a keyed project — and Core Web Vitals on this page are entirely Rela-controlled, so
  the number would be unactionable even if we had it. Do not call it; do not report it as a gap.
- The page has **three JSON-LD payloads** (since 2026-09-18): Rela's native static `Apartment`
  block, plus an injected `ApartmentComplex` block and an injected `RealEstateAgent` block, both
  from Advanced → Custom Script. The injected ones are assigned via `l.text = '{...}'` and must be
  extracted by regex on `l.text` — parsing `<script>` tags alone misses them.
- **Indexation is settled.** Search Console confirmed 2026-09-16: "URL is on Google", Indexed = 1,
  Not indexed = 0. Do not reopen it on the strength of a WebSearch miss — that tool has been shown
  three times over not to phrase-match or site-scope this domain.

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
`/llms.txt` populated, **and per-photo alt text** (added to this list 2026-09-18 — the Rela Photo
Gallery editor has no alt-text field at all; the only per-photo field is Description, which does not
emit an `alt` attribute, so all 19 gallery images render `alt=""`. It is platform-side, not an owner
task, and must not be re-listed as one).

**Scale check on the whole list above:** every item on it is a second-order on-page detail on a page
with zero inbound links. Shipping all of them would not change a ranking. Keep chasing Rela in one
consolidated message; do not let it consume Do-now slots that belong to link acquisition.

## Lifecycle

This monitors a **single listing**, which will eventually go under contract and sell. Tier 1
records `listing_status` every run. When it reports `pending` or `sold`, Tier 2 says so at the top
of the memo and recommends winding the routines down at https://claude.ai/code/routines. The
system is designed to end, not to run forever.
