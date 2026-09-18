# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Out-of-band rewrite, 2026-09-18.** This file is normally written only by Tier 2. It was rewritten
> here by a human-directed senior-SEO audit pass (see `reports/AUDIT-2026-09-18.md`) because three of
> its items were **factually stale** — they had been answered or closed by Tier 3 runs on 2026-09-16
> and 2026-09-18 whose findings never reached the queue (Tier 1 cannot observe them on the page, so
> Tier 2 never learned them). Tier 2 should adopt this state on its next run, not revert it.

## Do now

_(week of 2026-09-18 — the on-page work is finished. Everything below is off-page.)_

**The honest position:** the page is in good shape and has been byte-for-byte stable for three weeks.
It ranks for nothing because **nothing on the internet links to it** — verified again 2026-09-18: a
literal search for `"eastlakeview503.relahq.com"` returns exactly one result on the entire web, and
that result is this monitoring repo. More on-page polish will not change that. The three items below
are the whole job now.

### 1. Put the listing on your own Coldwell Banker Danforth page (5 minutes) — **highest value item on this list**

`https://omar-senghore.cbdanforth.com/` is live, it is yours, it already has a **"Featured Listing"**
section, and it mentions this property **zero times**. It is a real-estate-brand domain, it is
topically perfect, it is free, and it is almost certainly a followed link. This is the single best
inbound link available to this listing and it has never been asked for before today.

Log into whatever back-end manages that bio page (Coldwell Banker Danforth agent portal / Moxi) and
either set 1550 Eastlake Ave E #503 as the featured listing, or add this to the page body:

```
Now offered: 1550 Eastlake Ave E #503 — Riva Condominium
```

linked to `https://eastlakeview503.relahq.com/`, with this beneath it:

```
Top-floor 2 bed, 2 bath condo for sale at Riva Condominium in Seattle's Eastlake neighborhood, one block from Lake Union. 1,114 sq ft, Lake Union and skyline views, private balcony, 2 secured parking spaces plus storage. $649,888. MLS# 2556157.
```

Reply in Slack with "bio page done" so Tier 1 can confirm it next run.

### 2. Send two emails — both fully drafted, nothing to write (10 minutes)

**(a) To Coldwell Banker Danforth marketing / your managing broker.** Brokerage sites routinely link
an agent's single-property site. Copy-paste:

> Subject: Link for my 1550 Eastlake listing on the CB Danforth site
>
> Hi — I've got a single-property site up for my Eastlake listing and I'd like it linked from my
> agent page (and the listing page, if we have one) on cbdanforth.com.
>
> URL: https://eastlakeview503.relahq.com/
> Link text: 1550 Eastlake Ave E #503 — Riva Condominium
> MLS# 2556157, $649,888, 2 bed / 2 bath, 1,114 sq ft, Riva Condominium, Seattle 98102.
>
> Thanks,
> Omar

**(b) To urbnlivn.com** (Seattle condo blog — it already ranks on page 1 for "Riva Condos #503
Seattle" and "Riva Condominium Seattle for sale", which makes an editorial mention from them the
most valuable non-owned link realistically obtainable here). Use their site contact form or tips
address:

> Subject: Riva Condominium (1550 Eastlake) — top-floor unit just listed
>
> Hi — I'm the listing agent for 1550 Eastlake Ave E #503 at Riva Condominium in Eastlake, which
> just came on the market. Top floor, 2 bed / 2 bath, 1,114 sq ft, Lake Union and skyline views from
> a private balcony, two secured parking spaces plus storage. $649,888, MLS# 2556157. Built 1997,
> five floors, secured garage and lobby.
>
> You cover Riva regularly, so I thought it might be worth a mention. Full details and photos:
> https://eastlakeview503.relahq.com/
>
> Happy to send anything you need — floor plan, high-res photos, or a tour.
>
> Omar Senghore, Coldwell Banker Danforth (Everett) — 206-683-5030

Reply in Slack with "brokerage emailed" / "urbnlivn emailed".

### 3. Settle the name spelling (30 seconds) — **new, and it is a live inconsistency**

Verified on the live page 2026-09-18: it now carries **both** spellings at once — `Omar Senghor`
(×2, Rela's native `Apartment.provider.name` and the "Presented By" widget) and `Omar Senghore` (×1,
in the `RealEstateAgent` JSON-LD block added on 2026-09-18). Your Coldwell Banker bio page says
**Senghore**. Two spellings of the agent's name in the structured data of one page is a genuine
entity-consistency problem — it splits the signal that ties you, the brokerage and the listing
together.

Just reply in Slack: **"Senghor"** or **"Senghore"**. Whichever you say becomes the one spelling
everywhere, and fixing the other two places is a five-minute Tier 3 / Rela edit.

## Next up (not this week)

- **Link the JSON-LD nodes (`containedInPlace`)** *(carried 3 weeks)*. Confirmed still absent on the
  live page 2026-09-18 (`containedInPlace` appears 0 times). The unit node (`Apartment`) and the
  building node (`ApartmentComplex`) still are not connected, so Google is not told #503 sits inside
  Riva Condominium. **This is the only remaining item inside Tier 3's auto-save allowlist** — it is
  an additive Custom-Script JSON-LD edit using facts already in this repo. Worth doing precisely
  because it is free; it is not worth another week of memo space if it does not happen.
  *Caveat for whoever implements it:* Rela's native `Apartment` block carries no `@id`, so the link
  cannot be made by reference to it. The workable additive form is to give the injected
  `ApartmentComplex` node an `@id` and emit a small `Apartment` node carrying `containedInPlace`
  pointing at that `@id`. If that would duplicate the native `Apartment` node in a way that looks
  like conflicting markup, **draft it, do not auto-save it** — say so in the implementation report.

- **Chase Rela support** *(carried 3 weeks)*. One consolidated message, now including the alt-text
  item (below). Still outstanding: `twitter:card`, `og:url`, `og:locale`, H1 =
  "1550 Eastlake Ave E #503, Seattle, WA 98102" (currently "Apt 503, Seattle"), JSON-LD
  `numberOfBedrooms` (currently `numberOfRooms`), `amenityFeature` / `petsAllowed` /
  `containedInPlace` on the native node, `<img loading="lazy">`, `/sitemap.xml` = 200, `robots.txt`
  without `Crawl-delay: 10` and with a `Sitemap:` line, `/llms.txt` populated, **and per-photo alt
  text**. All confirmed still outstanding 2026-09-18.

- **Report the GSC Links number, once a month** *(new)*. Search Console → **Links** → "Top linking
  sites" → paste the external link count into Slack. Under a minute. This is the only authoritative
  measurement of the one number this whole system is built around; right now that number is
  *asserted* as zero every week, never *verified*.

## Closed / cut

- **✅ Search Console indexation — ANSWERED, stop asking.** Settled 2026-09-16 (recorded in
  `reports/IMPLEMENTATION-2026-09-16.md`): GSC showed **"URL is on Google"**, Page indexing **"Page
  is indexed"**, Indexing → Pages **Indexed = 1, Not indexed = 0**. The page is in Google's index.
  It was carried for two extra weeks only because Tier 3's answer had no route back into the
  baseline. **Do not re-open this on the strength of a WebSearch miss** — that tool has been
  demonstrated three times over not to phrase-match or site-scope this domain.

- **✅ `RealEstateAgent` JSON-LD node — DONE and live.** Applied 2026-09-18, independently
  re-verified on the live page 2026-09-18: `RealEstateAgent` present, `telephone
  "+1-206-683-5030"` present, `cbdanforth.com` URL present, `worksFor` → Coldwell Banker Danforth.
  The page now serves three JSON-LD payloads. Was carried three weeks as "blocked"; it is finished.

- **✂️ Photo alt text — CUT, platform-blocked, confirmed.** Settled 2026-09-18 inside the Rela Photo
  Gallery editor: the only per-photo field is **Description** (already filled for all 19 photos on
  2026-09-10) and it does not emit an `alt` attribute. All 19 gallery images still render `alt=""`.
  **There is no alt-text field to find.** Stop listing this as an owner task; it lives on the Rela
  support chase and nowhere else. (Scale check for whoever is tempted to re-escalate it: alt text on
  19 listing photos is a small image-search and accessibility win on a page that has zero inbound
  links. It was never going to move rankings.)

- **✅ Baseline page speed — CLOSED, and the check is now disabled.** Three consecutive 429s from a
  public quota of 0/day. As of 2026-09-18 the PageSpeed call is switched off in
  `state/competitors.json` (`pagespeed_skip: true`) so Tier 1 stops spending a request on it every
  week. Not worth asking the owner for an API key either: Core Web Vitals on this page are entirely
  Rela-controlled, so the number would be unactionable even if we had it.

- **✅ README Slack channel name — already fixed.** `README.md` says `#all-seo-eastlake`. This
  backlog item was itself stale.

- **✂️ Tracked query "Eastlake condo for sale Lake Union view" — RETIRED.** Unwinnable head term for
  a zero-authority orphan page; three runs of identical results, zero decisions. Removed from
  `state/competitors.json`.

- **✅ GA4 native-field item — CLOSED** (plan-locked; outcome achieved via Custom Script,
  `G-95JF0FLSZH` confirmed loading). No week counter.

- **ℹ️ Redfin $698,000 discrepancy — not ours to chase.** It came from a search-tool summary that has
  proven unreliable on this domain, about a third-party page we cannot fetch. Our own price is
  confirmed live at $649,888. If the owner wants certainty it is a 30-second look in a normal
  browser. Do not re-raise it as a finding.

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the
2026-09-10 through 2026-09-18 work (SEO & Social fields, property description rewrite, year built
1997, amenities 7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent`
JSON-LD). It was moved out of this file on 2026-09-18 — a queue that is two-thirds changelog stops
being read.
