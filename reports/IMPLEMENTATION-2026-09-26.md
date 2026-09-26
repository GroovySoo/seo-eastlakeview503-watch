# Tier 3 Implementation — 2026-09-26 (manual run, Claude in Chrome)

Run by hand at the owner's request, not on the Monday schedule. The `playwright` MCP server —
the standing Tier 3 browser since 2026-09-21 — **failed to connect this session**
(`CONNECT_TIMEOUT` after 30s), so no Playwright tools existed to call. Claude in Chrome was used
instead and worked for every step. See "Risk" below.

Listing status reconfirmed before touching anything: Rela dashboard shows **Published**, the live
page badge reads **Active**, price unchanged at $649,888. Not Sold/Pending — changes in scope.

## What this run closed: the surname question

Tier 3 logged "agent surname spelling — Senghor or Senghore?" as **needs info** on both 2026-09-18
and 2026-09-21. It is now answered from the owner's own brokerage record, not a guess. All three
authoritative sources agree on **Senghore**:

- Coldwell Banker Danforth broker admin, My Website → Contact Info: First `Omar`, Last `Senghore`
- The public agent site `https://omar-senghore.cbdanforth.com` (title, headings, contact block)
- That site's own `RealEstateAgent` JSON-LD: `"name": "Omar Senghore"`

`Senghor` on the listing was a typo in one Rela field, not a variant spelling.

## Summary table

| Item | Status | What changed (old → new) |
|---|---|---|
| Rela → Advanced → Custom Script: agent JSON-LD | **applied + verified** | email `change-re@outlook.com` → `i_give@hotmail.com`; added `@id`, `image`, `jobTitle`, NWMLS `identifier`, `areaServed`, `sameAs`. Block grew 1745 → 2187 chars. |
| Rela → Theme & Contacts → Listing Agent card: name | **applied + verified** | `Omar Senghor` → `Omar Senghore` |
| Rela agent card: email | **applied + verified** | `change-re@outlook.com` → `i_give@hotmail.com` |
| Rela agent card: title | **applied + verified** | empty → `Broker - Value-Add Real Estate Investment Specialist` |
| Rela agent card: phone | **applied + verified** | empty → `206-683-5030` |
| Rela agent card: company | **applied + verified** | empty → `Coldwell Banker Danforth (Everett)` |
| Rela agent card: website | **applied + verified** | empty → `https://omar-senghore.cbdanforth.com/` |
| WA licence number (`field_agent_bre`) | **skipped by owner** | left empty; owner chose "skip for now" |

Only the name and email were pre-approved edits to existing values. Title, phone, company and
website were **empty** fields filled from the brokerage record — additive, nothing overwritten.

## Why this mattered more than it looks

Google resolves an agent entity across sites by matching name, phone, email and URL. The listing
was claiming an agent called "Omar Senghor" at `change-re@outlook.com`, while the owner's real
brokerage presence is "Omar Senghore" at `i_give@hotmail.com` on
`omar-senghore.cbdanforth.com`. Those read as **two different people**, so none of the Coldwell
Banker site's authority could associate with this listing.

The injected block now carries `"@id": "https://omar-senghore.cbdanforth.com"` — the exact `@id`
the agent site publishes for itself — plus the NWMLS agent ID `NWM62208`. That is what binds the
two pages to one entity.

`change-re@outlook.com` is the **Rela account login address**, which is why it kept reappearing as
the agent email. Now overridden in both places.

## Verification (live page, cache-busted, after save)

```
"provider":{"@type":"RealEstateAgent","name":"Omar Senghore",
            "telephone":"206-683-5030","email":"i_give@hotmail.com"}
```

- `Senghore` present: **yes**
- `Senghor` (typo) occurrences: **0**
- `change-re@outlook.com` present: **no**
- `i_give@hotmail.com` present: **yes**
- GA4 tag `G-95JF0FLSZH` still intact: **yes** (checked explicitly — the script edit sat in the
  same field as the analytics tag)

The static `provider` node also picked up the phone number automatically from the agent card.

## Inbound links — a target was identified

`https://omar-senghore.cbdanforth.com` is live, owner-controlled, on a Coldwell Banker subdomain,
and has a "Featured Listing" section. It remains the best available inbound link and is still
**owner-only** (separate portal, owner's identity). Unchanged from previous runs, but now the
agent-side identity matches, so a link from there will carry entity weight rather than pointing
at a stranger.

## Still missing (owner action)

- **WA licence number** — `Lic #` empty in broker admin and `field_agent_bre` empty in Rela.
  Strongest remaining trust signal for an agent entity; it is public record.
- **Social profiles** — every social URL field in broker admin is blank, which is why the agent
  site's own `sameAs` array is five empty strings.
- **Qualifications** section on the agent site is empty.

## Risk: Tier 3's browser

The scheduled Monday run is configured for the `playwright` MCP server, which did not connect
today. If that persists, the automated run will fail the way the 2026-09-21 Chrome run did.
Either fix that server or switch the task back to Claude in Chrome, which handled every step of
this run without issue.

## Suspicious content

None. Pages were read strictly as data. Note for the record: the Rela sign-in form arrived with
the owner's credentials pre-filled by the browser password manager; the agent did not submit it —
the owner signed in personally, then handed control back.
