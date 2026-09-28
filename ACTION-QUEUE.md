# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-09-28.** Status changes below come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-09-28.md` (live-page observation), not from assumption. Also folds
> in out-of-band knowledge from `reports/IMPLEMENTATION-2026-09-26-run2.md` that can never appear on
> the page: the Search Console **Links** report has finished processing and reads **External links: 0,
> Top linking sites: No data**. That is the first authoritative measurement of the inbound-link count
> and it is now recorded in `state/last-snapshot.json`.

## Do now

_(week of 2026-09-28 — the on-page work is finished. Everything below is off-page and owner-only.)_

**The honest position, now confirmed by Google:** external links to this listing = **0**
(Search Console → Links, read 2026-09-26). Third-party mentions = **0**, unchanged on every run since
2026-09-10. The page is technically sound, indexed, and has been stable for six weeks. It ranks for
nothing because nothing on the web points at it. No further on-page polish will change that.

**Both items below have now carried three weeks.** They are not hard — the click path and both emails
are already written, and the whole list is about 15 minutes. They are owner-only, because each one
publishes or sends as the owner. So the list has been **cut down rather than repeated**: the single
highest-value item goes first and alone, and item 1 now has an explicit "I'm blocked" reply so a
silent stall becomes a solvable problem instead of a fourth carried week.

### 1. Put the listing on your own Coldwell Banker Danforth page (5 minutes) — **highest value item on this list** *(carried 3 weeks)*

`https://omar-senghore.cbdanforth.com/` is live, it is yours, it already has a **"Featured Listing"**
section, and re-checked on 2026-09-28 it mentions this property **zero times**. Real-estate brand
domain, topically perfect, free, almost certainly a followed link. Best inbound link available
(`state/competitors.json` → `link_targets`, rank 1).

Click path:

1. Sign in to the Coldwell Banker Danforth agent portal (the Moxi admin behind the bio page).
2. **My Website → Featured Listing** (may read "Featured Property").
3. Set it to **1550 Eastlake Ave E #503** and save.

If the listing cannot be picked from a menu, paste this into the page body instead, with the first
line linked to `https://eastlakeview503.relahq.com/`:

```
Now offered: 1550 Eastlake Ave E #503 — Riva Condominium
```

```
Top-floor 2 bed, 2 bath condo for sale at Riva Condominium in Seattle's Eastlake neighborhood, one block from Lake Union. 1,114 sq ft, Lake Union and skyline views, private balcony, 2 secured parking spaces plus storage. $649,888. MLS# 2556157.
```

Reply in Slack with **"bio page done"** so Tier 1 can confirm it live next run.

**New this week — the escape hatch.** If the portal login or that screen cannot be found, reply
**"bio page blocked — can't get in"**. That is a useful answer: it converts this from a carrying task
into one we route around by asking the brokerage to make the change instead.

### 2. Email Coldwell Banker Danforth marketing / the managing broker — fully drafted (3 minutes) *(carried 3 weeks)*

Brokerage sites routinely link an agent's single-property site. Supporting argument, unchanged since
2026-09-26: `coldwellbankerhomes.com` — Coldwell Banker's own national site — ranks for
"Riva Condominium Seattle for sale" while this listing does not. The brand family already ranks for
this building. Copy-paste:

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

Reply in Slack with **"brokerage emailed"**.

### 3. Email urbnlivn.com — fully drafted (3 minutes) *(carried 3 weeks)* — **target upgraded back to rank 3 this week**

Use their site contact form or tips address.

**Correction to last week's note:** 2026-09-26 downgraded this target because urbnlivn had dropped out
of all four tracked queries. It is **back** in the returned set for "Riva Condos #503 Seattle" as of
2026-09-28, so that downgrade was premature. It is again a site that ranks for the exact building name,
which is the whole reason it sits at rank 3 in `link_targets`.

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

Reply in Slack with **"urbnlivn emailed"**. If it goes nowhere, the next target is the **Eastlake
Community Council** (`https://www.eastlakeseattle.org/`, `link_targets` rank 4); that ask gets drafted
when this one is spent, not piled on alongside it.

**Not asked this week: the Search Console links number.** It was read on 2026-09-26 and the answer is
**0** — see "Done". Next monthly ask falls on the first run of October.

## Next up (not this week)

- **Add your WA real-estate licence number** (~2 minutes, two places). Empty in the Coldwell Banker
  broker admin (`Lic #`) and empty in Rela (`field_agent_bre`); marked "skip for now" by the owner on
  2026-09-26. It is public record and it is the strongest remaining trust signal for an agent entity
  now that the name, email and NWMLS ID all line up. Small but genuinely cheap.
- **Fill in the social-profile fields in the Coldwell Banker broker admin.** They are all blank, which
  is why the bio site's own `sameAs` array publishes five empty strings. Small effect, low effort.
- **Make the phone number format consistent.** Rela's native block emits `206-683-5030`; the injected
  agent block emits `+1-206-683-5030`. Both correct, one is not E.164. A two-character Tier 3 edit;
  slightly tightens the entity match that the 2026-09-26 work just built. Not worth a dedicated run.
- **Tier 3 browser reliability (maintainer task, not the owner's).** `playwright` MCP timed out on
  2026-09-26; the Claude in Chrome extension failed on 2026-09-21. Each run has only succeeded because
  the other browser happened to work. This will eventually cost a week of implementation. Pick one
  browser and make it the reliable one.

## Backlog / blocked

- **Chase Rela support (the 8-item bundle) — MOVED TO BACKLOG 2026-09-26, as scheduled** *(was carried
  5 weeks)*. Last week set an explicit cut-off: "if this is not sent by 2026-09-25 it moves to Backlog
  / blocked and stops being listed." It is 2026-09-26 with no confirmation it was sent, so it stops
  being listed weekly. **Do not re-list it in "Do now".** Every item in it is cosmetic or entirely
  platform-controlled, and none of them is why this page doesn't rank. The message is preserved below
  and can be sent at any time in one paste:

  > Hi — I run a single-property site on Rela (eastlakeview503.relahq.com) and there are a few
  > SEO items I can't reach from the editor. Could you get these in front of the product team?
  >
  > 1. `/sitemap.xml` returns 404 — there is no sitemap for the site.
  > 2. `robots.txt` has `Crawl-delay: 10` and no `Sitemap:` line.
  > 3. `/llms.txt` returns the normal page HTML instead of llms.txt content.
  > 4. No per-photo alt text: the Photo Gallery editor only has a Description field, and it doesn't
  >    become an `alt` attribute — all 19 listing photos render `alt=""`.
  > 5. Missing social tags: `og:url`, `og:locale`, `twitter:card`.
  > 6. The H1 reads "1550 Eastlake Ave E Apt 503, Seattle" — I'd like "1550 Eastlake Ave E #503,
  >    Seattle, WA 98102".
  > 7. Listing structured data uses `numberOfRooms` rather than `numberOfBedrooms`, and has no
  >    `amenityFeature`, `petsAllowed` or `containedInPlace`.
  > 8. Listing photos have no `loading="lazy"`.
  >
  > Thanks — happy to give any detail you need.

  All 8 items re-confirmed still outstanding on the live page 2026-09-28, unchanged.

- **Link the structured-data blocks (`containedInPlace`) — STILL BACKLOG, blocker partially lifted
  2026-09-26** *(was carried 4 weeks)*. Confirmed absent again 2026-09-28 (0 occurrences site-wide).
  **Update:** the specific technical blocker recorded here no longer holds — Rela's native `Apartment`
  block now carries `@id: "https://eastlakeview503.relahq.com#listing"`, which appeared on its own
  this week without being asked for. However the building node (`ApartmentComplex`) still has **no
  `@id`** to point at, so the link still cannot be made cleanly by reference, and on a page with zero
  inbound links the upside remains indistinguishable from zero. **Recording the change; deliberately
  not promoting it.** It reopens if Rela also adds an `@id` to the `ApartmentComplex` block. Side
  benefit of the observation: Rela is evidently still shipping template changes, which is mildly
  encouraging for the support-chase items above.

## Done

- **✅ Search Console "Links" number read — DONE 2026-09-26, the first verified inbound-link count.**
  Out-of-band knowledge from `reports/IMPLEMENTATION-2026-09-26-run2.md`; it can never be observed on
  the live page, so the certification rule does not apply — this was a **read**, not a change to the
  site. Tier 3 opened Search Console → Links for `https://eastlakeview503.relahq.com/` (URL-prefix
  property) and the report had finished processing: **External links total 0. Top linking sites:
  No data. Top linking text: No data. Internal links: 0.** The 2026-09-21 "Processing data, please
  check again in a day or so" banner is gone. This agrees exactly with Tier 1's search-based figure and
  retires the standing caveat that zero was asserted weekly but never verified. **It is a real zero.**
  Carried as an ask since 2026-09-21; finished. Recorded in `state/last-snapshot.json`
  (`inbound_links.gsc_top_linking_sites_status`, `external_links_verified`). The monthly re-ask resumes
  on the first run of October.

- **✅ Agent name spelling settled — DONE 2026-09-26.** Decided from the owner's own brokerage record
  rather than guessed: Coldwell Banker Danforth broker admin (My Website → Contact Info) reads
  First `Omar` / Last `Senghore`, matching the public bio site and that site's own `RealEstateAgent`
  structured data. `Senghor` on the listing was a typo in one Rela field, not a variant spelling.
  Applied by Tier 3 and **independently confirmed live by Tier 1 the same day**: all 4 sitewide
  occurrences read "Omar Senghore", 0 read "Omar Senghor", and the visible "Presented By" widget
  matches the structured data. Carried 2 weeks; finished.

- **✅ Agent identity reconciled across sites — DONE 2026-09-26.** Not previously a numbered queue
  item; recorded here because Tier 1 confirmed it live and it is the week's substantive win. The
  listing's agent email moved from `change-re@outlook.com` (which was the **Rela account login
  address** leaking into the agent field) to the address on the owner's brokerage record, in all 3
  places it appears. The injected `RealEstateAgent` block also gained `@id`
  (`https://omar-senghore.cbdanforth.com` — the exact `@id` the bio site publishes for itself),
  `jobTitle`, `image`, NWMLS `identifier` `NWM62208`, `areaServed` and `sameAs`. The Rela agent card's
  empty title / phone / company / website fields were filled from the brokerage record (additive —
  nothing overwritten). GA4 tag `G-95JF0FLSZH` verified still loading afterwards by both Tier 3 and
  Tier 1, because the edit shared a field with the analytics tag. Effect: the listing and the
  brokerage site now describe one person rather than two.

- **✅ `RealEstateAgent` structured-data block — DONE 2026-09-18**, and further enriched 2026-09-26
  (see above). Confirmed live by Tier 1 on both dates. The page now serves three structured-data
  payloads.

## Closed / cut

- **✅ Search Console indexation — ANSWERED, stop asking.** Settled 2026-09-16 (recorded in
  `reports/IMPLEMENTATION-2026-09-16.md`): GSC showed **"URL is on Google"**, Page indexing **"Page
  is indexed"**, Indexing → Pages **Indexed = 1, Not indexed = 0**. The page is in Google's index.
  Recorded in `state/last-snapshot.json` (`indexed: "yes (GSC 2026-09-16)"`), so it can stop being
  rediscovered. **Do not re-open this on the strength of a WebSearch miss** — that tool has been
  demonstrated four times over not to phrase-match or site-scope this domain. Per the 2026-09-18 scope
  change, Tier 1 no longer runs the verbatim-phrase check at all; only a fresh GSC reading or a
  listing-status change would justify revisiting it.

- **✂️ Photo alt text — CUT, platform-blocked, confirmed.** Settled 2026-09-18 inside the Rela Photo
  Gallery editor: the only per-photo field is **Description** (already filled for all 19 photos on
  2026-09-10) and it does not emit an `alt` attribute. All 19 gallery images still render `alt=""`.
  **There is no alt-text field to find.** Stop listing this as an owner task; it lives on the Rela
  support chase and nowhere else. (Scale check: alt text on 19 listing photos is a small image-search
  and accessibility win on a page that has zero inbound links. It was never going to move rankings.)

- **✅ Baseline page speed — CLOSED, and the check is now disabled.** Three consecutive 429s from a
  public quota of 0/day. As of 2026-09-18 the PageSpeed call is switched off in
  `state/competitors.json` (`pagespeed_skip: true`) so Tier 1 stops spending a request on it every
  week. Not worth asking the owner for an API key either: Core Web Vitals on this page are entirely
  Rela-controlled, so the number would be unactionable even if we had it.

- **✅ README Slack channel name — already fixed.** `README.md` says `#all-seo-eastlake`.

- **✂️ Tracked query "Eastlake condo for sale Lake Union view" — RETIRED.** Unwinnable head term for
  a zero-authority orphan page; three runs of identical results, zero decisions. Removed from
  `state/competitors.json`.

- **✅ GA4 native-field item — CLOSED** (plan-locked; outcome achieved via Custom Script,
  `G-95JF0FLSZH` confirmed loading). No week counter.

- **ℹ️ Redfin $698,000 discrepancy — not ours to chase.** It came from a search-tool summary that has
  proven unreliable on this domain, about a third-party page we cannot fetch. Our own price is
  confirmed live at $649,888. Do not re-raise it as a finding.

- **ℹ️ Email signature and LinkedIn "Featured" links — NOT link targets.** No crawler sees an email
  signature; LinkedIn Featured links are nofollow and client-rendered. Fine for human traffic, never
  counted toward the link goal. See `state/competitors.json` →
  `link_targets.explicitly_not_link_targets`.

- **ℹ️ New `og:image:url` / `og:image:secure_url` tags (appeared 2026-09-26) — no action.** Both
  duplicate the existing `og:image`. Platform-side, cosmetic, harmless. Recorded so it is not
  rediscovered as a change next week.

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the
2026-09-10 through 2026-09-26 work (SEO & Social fields, property description rewrite, year built
1997, amenities 7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent`
JSON-LD, agent identity reconciliation).
