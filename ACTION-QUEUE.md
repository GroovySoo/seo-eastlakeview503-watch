# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-09-26.** Status changes below come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-09-26.md` (live-page observation), not from assumption. Also folds
> in out-of-band knowledge from `reports/IMPLEMENTATION-2026-09-26.md` and
> `reports/IMPLEMENTATION-2026-09-21.md` that can never appear on the page: the surname decision, the
> Search Console Links report still processing on Google's side, the empty WA licence number, and the
> blank social-profile fields. Those are now recorded in `state/last-snapshot.json` too.

## Do now

_(week of 2026-09-26 — the on-page work is finished. Everything below is off-page.)_

**The honest position, measured again this week:** third-party mentions of the domain = **0**,
unchanged on every run since 2026-09-10. The page is in good shape and has been stable for five
weeks. It ranks for nothing because nothing links to it. More on-page polish will not change that.

**What did change this week:** the listing's agent identity now matches the owner's real brokerage
identity (name, email, `@id`, NWMLS number). Before this, a link from the Coldwell Banker bio page
would have joined two apparent strangers. It no longer would. That makes item 1 more valuable than it
was last week, not less.

### 1. Put the listing on your own Coldwell Banker Danforth page (5 minutes) — **highest value item on this list** *(carried 2 weeks)*

`https://omar-senghore.cbdanforth.com/` is live, it is yours, it already has a **"Featured Listing"**
section, and re-checked on 2026-09-26 it mentions this property **zero times**. It is a real-estate
brand domain, topically perfect, free, and almost certainly a followed link. This is the single best
inbound link available to this listing (`state/competitors.json` → `link_targets`, rank 1).

Log into the Coldwell Banker Danforth agent portal (Moxi) that manages that bio page and either set
1550 Eastlake Ave E #503 as the featured listing, or add this to the page body:

```
Now offered: 1550 Eastlake Ave E #503 — Riva Condominium
```

linked to `https://eastlakeview503.relahq.com/`, with this beneath it:

```
Top-floor 2 bed, 2 bath condo for sale at Riva Condominium in Seattle's Eastlake neighborhood, one block from Lake Union. 1,114 sq ft, Lake Union and skyline views, private balcony, 2 secured parking spaces plus storage. $649,888. MLS# 2556157.
```

Reply in Slack with "bio page done" so Tier 1 can confirm it next run.

### 2. Send two emails — both fully drafted, nothing to write (10 minutes) *(carried 2 weeks)*

**(a) To Coldwell Banker Danforth marketing / your managing broker.** Brokerage sites routinely link
an agent's single-property site. New this week: `coldwellbankerhomes.com` — Coldwell Banker's own
national site — appeared in the results for "Riva Condominium Seattle for sale" for the first time.
Your own brand family already ranks for this building. Copy-paste:

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

**(b) To urbnlivn.com** (Seattle condo blog). Use their site contact form or tips address:

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

**Target-quality note on (b):** urbnlivn.com has now dropped out of the returned results for **all
four** tracked queries (it was on two of them on 2026-09-18). It is weaker than when it was ranked #3
in `link_targets`. Send it anyway — the text is already written, so it costs nothing. If it goes
nowhere, the next target is the **Eastlake Community Council** (`https://www.eastlakeseattle.org/`,
`link_targets` rank 4); that ask gets drafted next week rather than piled on this week.

Reply in Slack with "brokerage emailed" / "urbnlivn emailed".

### 3. Read the Search Console links number (under a minute) — **monthly ask, now unblocked**

Search Console → **Links** → **"Top linking sites"** → paste the total external-link count (and any
domains listed) into Slack.

**Why this is live again rather than carried:** on 2026-09-21 Tier 3 opened this exact report and
Google itself displayed *"Processing data, please check again in a day or so."* No number was withheld
or guessed — Google had not finished computing link data for this property. Five days have passed, so
it should now render.

This is the only authoritative measurement of the one number this whole system is built around. Right
now it is *asserted* as zero every week from a web search and has never once been *verified*.

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

  All 8 items re-confirmed still outstanding on the live page 2026-09-26, unchanged.

- **Link the structured-data blocks (`containedInPlace`) — STILL BACKLOG, blocker partially lifted
  2026-09-26** *(was carried 4 weeks)*. Confirmed absent again this week (0 occurrences site-wide).
  **Update:** the specific technical blocker recorded here no longer holds — Rela's native `Apartment`
  block now carries `@id: "https://eastlakeview503.relahq.com#listing"`, which appeared on its own
  this week without being asked for. However the building node (`ApartmentComplex`) still has **no
  `@id`** to point at, so the link still cannot be made cleanly by reference, and on a page with zero
  inbound links the upside remains indistinguishable from zero. **Recording the change; deliberately
  not promoting it.** It reopens if Rela also adds an `@id` to the `ApartmentComplex` block. Side
  benefit of the observation: Rela is evidently still shipping template changes, which is mildly
  encouraging for the support-chase items above.

## Done

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
