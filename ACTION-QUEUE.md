# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-09-18** (regular weekly pass), adopting the out-of-band audit state from
> earlier the same day (`reports/AUDIT-2026-09-18.md`) rather than reverting it, and folding in the
> Tier 3 findings from `reports/IMPLEMENTATION-2026-09-18.md` — the Search Console indexation
> reading, the confirmed absence of any alt-text field in the Rela editor, and the now-live
> `RealEstateAgent` block. Those are now also recorded in `state/last-snapshot.json`.

## Do now

_(week of 2026-09-18 — the on-page work is finished. Everything below is off-page.)_

**The honest position, measured again this week:** a literal web search for
`"eastlakeview503.relahq.com"` returns exactly one result on the entire internet, and that result is
this monitoring repository. Third-party mentions: **0**. The page itself is in good shape and has
been stable for four weeks. It ranks for nothing because nothing links to it. More on-page polish
will not change that.

### 1. Put the listing on your own Coldwell Banker Danforth page (5 minutes) — **highest value item on this list** *(carried 1 week)*

`https://omar-senghore.cbdanforth.com/` is live, it is yours, it already has a **"Featured Listing"**
section, and re-checked on 2026-09-18 it mentions this property **zero times**. It is a real-estate
brand domain, topically perfect, free, and almost certainly a followed link. This is the single best
inbound link available to this listing.

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

### 2. Send two emails — both fully drafted, nothing to write (10 minutes) *(carried 1 week)*

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

**(b) To urbnlivn.com** (Seattle condo blog). Still our best non-owned target: it ranks on page 1 for
"Riva Condominium Seattle for sale". Note it dropped out of the results for "Riva Condos #503
Seattle" this week — slightly less valuable than last week, still the best available. Use their site
contact form or tips address:

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

### 3. Settle the name spelling (30 seconds) *(carried 1 week)*

Re-verified on the live page 2026-09-18: it carries **both** spellings at once — `Omar Senghor` (×2,
Rela's native listing data and the "Presented By" widget) and `Omar Senghore` (×1, in the
`RealEstateAgent` block added 2026-09-18). Your Coldwell Banker bio page says **Senghore**. Two
spellings of the agent's name in one page's structured data splits the signal that ties you, the
brokerage and the listing together.

Reply in Slack with one word: **"Senghor"** or **"Senghore"**. Whichever you say becomes the one
spelling everywhere; fixing the other two places is a five-minute Tier 3 / Rela edit.

### 4. Small verification task — report the Search Console links number (under a minute)

Search Console → **Links** → **"Top linking sites"** → paste the total external-link count (and any
domains listed) into Slack. This is the only authoritative measurement of the one number this whole
system is built around; right now it is *asserted* as zero every week and has never been *verified*.
Monthly ask — first time it has been raised.

## Next up (not this week)

- **Chase Rela support** *(carried 4 weeks — broken down, last chance as a live item)*. This kept
  getting carried because it was written as "chase Rela about twelve things", which nobody does on a
  Tuesday. There is now nothing to compose — send this as one message via Rela support/chat:

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

  If this is not sent by 2026-09-25 it moves to Backlog / blocked and stops being listed.

- **Report the GSC Links number, monthly.** Promoted to "Do now" item 4 this week because it has
  never actually been done once. Returns here as a monthly item after the first report.

## Backlog / blocked

- **Link the structured-data blocks (`containedInPlace`) — BLOCKED as of 2026-09-18** *(was carried
  4 weeks)*. Confirmed absent again this week (0 occurrences site-wide): the unit node (`Apartment`)
  and the building node (`ApartmentComplex`) are still unconnected. It is blocked for a real
  technical reason, not neglect: Rela's native `Apartment` block carries no `@id`, so the link cannot
  be made by reference to it. The only additive workaround is to emit a second `Apartment` node
  carrying `containedInPlace`, which risks reading as duplicate/conflicting markup. On a page with
  zero inbound links the upside is close to zero either way. **Do not re-list it weekly.** It
  reopens if Rela adds `@id` to the native block, or if it can be drafted (not auto-saved) and
  reviewed as a one-off.

## Done

- **✅ `RealEstateAgent` structured-data block — DONE 2026-09-18.** Applied by Tier 3 and
  independently confirmed live on the page by Tier 1 the same day: `RealEstateAgent` present,
  `telephone "+1-206-683-5030"`, the `cbdanforth.com` bio URL, `worksFor` → Coldwell Banker Danforth
  (Everett, WA). The page now serves three structured-data payloads. Carried three weeks as
  "blocked"; finished.

## Closed / cut

- **✅ Search Console indexation — ANSWERED, stop asking.** Settled 2026-09-16 (recorded in
  `reports/IMPLEMENTATION-2026-09-16.md`): GSC showed **"URL is on Google"**, Page indexing **"Page
  is indexed"**, Indexing → Pages **Indexed = 1, Not indexed = 0**. The page is in Google's index.
  Now also recorded in `state/last-snapshot.json` (`indexed: "yes (GSC 2026-09-16)"`), so it can
  stop being rediscovered. **Do not re-open this on the strength of a WebSearch miss** — that tool
  has been demonstrated four times over not to phrase-match or site-scope this domain.

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

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the
2026-09-10 through 2026-09-18 work (SEO & Social fields, property description rewrite, year built
1997, amenities 7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent`
JSON-LD).
