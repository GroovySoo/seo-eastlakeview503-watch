# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-10-19.** Live-page status changes come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-10-19.md`, not from assumption. **No new Tier 3 implementation
> report since the last rewrite** (newest is `reports/IMPLEMENTATION-2026-10-05.md`, already folded in
> on 2026-10-12), so there is no new out-of-band knowledge to import this week. Two changes made on
> Tier 2's own judgement, both documented in `reports/STRATEGY-2026-10-19.md`: the licence-number item
> is **retired to Backlog** under its own once-only re-raise rule, and the **Eastlake Community
> Council** email is promoted into its slot. Standing blockers unchanged: the Coldwell Banker broker
> admin is signed out, so whether a "Virtual Tour" field exists on the MLS #2556157 listing card is
> still unknown.

## ⭐ Milestone: the first inbound link is live and holding

`https://omar-senghore.cbdanforth.com/` carries
`<a href="https://eastlakeview503.relahq.com/">1550 Eastlake Ave E #503 — Riva Condominium, Seattle.</a>`
in its About Me section — **followed**, no `rel="nofollow"`, server-rendered. Verified by Tier 1 on
2026-10-05 and **re-verified byte-identical on 2026-10-12 and again on 2026-10-19** — three
consecutive weeks holding. External links: **0 → 1**.

Three measures still disagree, and all three stay recorded rather than collapsing into the flattering
one:

| Measure | Reading | Worth |
|---|---|---|
| Tier 1 direct fetch | **1** | Authoritative. Re-confirmed 2026-10-19. |
| Weekly automated mention search | 0 | A floor. Has never been able to see this domain. |
| Search Console → Links (2026-10-05) | 0 | Real but lagging — Google has not re-crawled the bio page since the link went live 2026-09-28. |

**A Search Console 0 at this stage is not a problem and needs no action.** Next reading due the first
run of November.

## Do now

_(week of 2026-10-19 — all on-page work is finished; everything below is off-page. The page has now
been byte-for-byte unchanged for three consecutive weeks, which is the correct state.)_

### 1. Add the listing site as the "Virtual Tour" link on your Coldwell Banker listing (~3 minutes) — **highest value item on this list** *(carried 2 weeks)*

This is inbound link **#2** from the same strong real-estate domain that gave us link #1. Your CB
listing page for #503 links to Coldwell Banker's own detail page but not to your site.

**Why it still has not happened:** the broker admin is **signed out**, and Tier 3 never submits a
login form. It reached the login screen on 2026-10-05 and stopped. Nothing was changed and the listing
card was never opened — so the field may or may not exist. Tier 1 re-checked the public bio page on
2026-10-19 and it contains no "Virtual Tour" text and no link to any cbdanforth.com listing-detail
page, which is not conclusive either way: that bio page is not the listing card. **This item cannot
move without one action from the owner** — either Option A or the single word in Option B.

**Option A — do it yourself (3 minutes):**

1. Go to `https://www.cbdanforth.com/` and click **Broker Login**, and sign in.
2. **My Website → Listings**, find the card for **MLS #2556157**.
3. Open it for editing and look for a field labelled **Virtual Tour**, **Virtual Tour URL**,
   **Tour Link** or **Property Website**.
4. Paste exactly this into that field, and save:

```
https://eastlakeview503.relahq.com/
```

Reply in Slack with **"virtual tour done"** so Tier 1 can confirm it live next run.

**Option B — sign in and hand it off.** Sign in at the same place, then reply in Slack with
**"CB signed in"**. Next Monday's run makes the edit for you.

**Escape hatch:** if there is no such field on the listing card, reply **"no virtual tour field"**.
That closes the item for good instead of carrying it.

### 2. Email urbnlivn.com — fully drafted, recipient now looked up (~3 minutes) *(carried 6 weeks — the oldest open item; broken into a smaller step 2026-10-19)*

Rank 3 in `state/competitors.json` → `link_targets`: a Seattle condo blog that covers the Riva
building. An editorial mention from a site that already ranks for the exact building name is the
highest-quality non-owned link realistically obtainable here.

**Carried-6-weeks note (2026-10-19).** The draft below cannot usefully be cut down further, so instead
of re-listing it unchanged a seventh time, the remaining friction — "who do I send it to?" — has been
removed. Looked up and verified live on 2026-10-19:

- **Send to: `matt@urban-living.com`.** urbnlivn.com publishes three addresses on its homepage —
  `matt@urban-living.com`, `alicia@urban-living.com`, `land@urban-living.com`. The blog is published
  by **Urban Living, a Seattle condo brokerage**, so these are the editorial side.
- **Also paste it into the form at `https://www.urbnlivn.com/contact-us`** (HTTP 200, verified today).
  Belt and braces; costs ten seconds.
- **Confirmed on the merits today:** their homepage mentions "Riva" **three times**. The building
  genuinely is on their beat — this is not a cold generic pitch.
- **They are a competing brokerage, so the draft leads with the building, not with your listing.**
  That framing is deliberate. Do not rewrite it into a "please promote my listing" ask.

If they say no, reply **"urbnlivn declined"** and the item closes for good rather than carrying a
seventh week.

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

Reply in Slack with **"urbnlivn emailed"** — or **"urbnlivn declined"** if they turn it down.

**Do not re-rank this target on search movement.** 2026-09-26 downgraded it because it left the
tracked queries, 2026-09-28 upgraded it because it came back, and it has been absent from all four
since 2026-10-05. The tracked-query tool is too volatile on this domain to rank targets by; this
target is ranked on the merits.

### 3. Email the Eastlake Community Council — fully drafted, address looked up (~3 minutes) *(promoted from "Next up" 2026-10-19)*

Promoted into the slot freed by retiring the licence-number item (see Backlog). Rank 4 in
`state/competitors.json` → `link_targets`: a hyper-local, topically relevant neighbourhood domain.
Local-community links are exactly the kind a single-listing microsite can realistically earn, and this
one is an entirely different kind of domain from the two real-estate sites above, which is good for a
link profile that currently has exactly one link in it.

**Send to: `info@eastlakeseattle.org`** — published on `https://www.eastlakeseattle.org/` (HTTP 200,
verified 2026-10-19). Paste this:

> Subject: Riva Condominium (1550 Eastlake Ave E) — resident-interest listing in the neighbourhood
>
> Hi — I'm a Coldwell Banker Danforth broker working in Eastlake, and I'm handling the sale of a
> top-floor unit at Riva Condominium, 1550 Eastlake Ave E. Built 1997, five floors, secured garage and
> lobby — one of the quieter buildings on that stretch, a block from Lake Union.
>
> If the Council keeps a neighbourhood news page, a local-listings roundup, or a newsletter section
> where this would fit, I've put full details, photos and floor information here:
> https://eastlakeview503.relahq.com/
>
> I'd also be glad to help out as a local business — happy to hear what the Council needs this year.
>
> Omar Senghore, Coldwell Banker Danforth (Everett) — 206-683-5030

Reply in Slack with **"ECC emailed"** — or **"ECC declined"** and it closes.

**Framing note:** this is a neighbourhood-interest and local-business ask, not a link request. Do not
rewrite it into "please link to my site" — community sites decline those, and the offer of help is the
part that actually opens the door.

## Next up (not this week)

- **Zillow / Realtor.com agent profile "website" field** (`link_targets` rank 5, owner-controlled,
  ~5 min each). **Frame as referral traffic, never as a link** — both are nofollow and must not be
  counted toward the link goal.
- **Fill in the social-profile fields in the Coldwell Banker broker admin.** All blank, which is why
  the bio site's own `sameAs` array publishes five empty strings. Small effect, low effort.
- **Make the phone number format consistent.** Rela's native block emits `206-683-5030`; the injected
  agent block emits `+1-206-683-5030`. Both correct, one is not E.164. A two-character Tier 3 edit;
  not worth a dedicated run.
- **Tier 3 browser reliability (maintainer task, not the owner's).** Claude in Chrome worked cleanly
  on 2026-10-05 — connected first call, navigated and closed its tab — the third consecutive clean
  data point, after `playwright` MCP timed out 2026-09-26 and Chrome disconnected mid-session
  2026-09-28. Standing workarounds to keep recorded: prefer an element's own JS `click()` over mouse
  coordinates in the CB admin (coordinates signed the owner out twice); `javascript_tool` is blocked
  whenever a returned value contains a URL with a query string, so return `{origin, pathname,
  hasQuery}` instead of a raw href; Search Console accepts a direct deep link to the Links report with
  the property pre-selected, which skips the property picker.

## Backlog / blocked

- **Add your Washington real-estate licence number — RETIRED TO BACKLOG 2026-10-19** *(was carried 2
  weeks in "Do now")*. **Do not re-list it in "Do now".** The owner replied **"skip for now"** on
  2026-09-26. It was re-raised once on 2026-10-12 as a cheap trust signal, under an explicit
  once-only rule, and no reply came; Tier 1 re-confirmed on 2026-10-19 that no licence number appears
  anywhere in the live page's agent data. A third listing would cost the weekly list credibility for a
  low-value item, so it is retired on the owner's original answer. **It is still worth doing** and
  reopens the moment the owner wants it — reply **"licence added"** and Tier 1 will confirm the Rela
  side on the live page next run. Two labelled fields, same number in both:

  1. Coldwell Banker Danforth broker admin → **My Website → Contact Info** → field marked **Lic #**.
  2. Rela editor → **Theme & Contacts** → field marked **field_agent_bre**.

- **Email Coldwell Banker Danforth marketing / the managing broker — MOVED TO BACKLOG 2026-10-12**
  *(was carried 5 weeks)*. **Do not re-list it in "Do now".** It was cut down twice — full draft, then
  "just name a recipient" — and moved neither time, which says the blocker is real and outside the
  owner's control: there is no known marketing contact at the brokerage and nothing on this list can
  manufacture one. It also aims at the same prize as "Do now" item 1 (a link on a Coldwell Banker
  domain) by a route that depends on a third party, where item 1 depends on nobody. Reopens the moment
  the owner learns a recipient — reply **"brokerage contact: <name or email>"** and it goes straight
  back to "Do now". Supporting argument, unchanged: `coldwellbankerhomes.com` ranks for "Riva
  Condominium Seattle for sale" while this listing does not. The draft is preserved:

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

- **Chase Rela support (the 8-item bundle) — IN BACKLOG since 2026-09-26** *(was carried 5 weeks)*.
  **Do not re-list it in "Do now".** Every item in it is cosmetic or entirely platform-controlled, and
  none of them is why this page doesn't rank. All 8 re-confirmed still outstanding on the live page
  2026-10-19, unchanged. The message is preserved and can be sent at any time in one paste:

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

- **Link the structured-data blocks (`containedInPlace`) — STILL BACKLOG** *(was carried 4 weeks)*.
  Confirmed absent again 2026-10-19 (0 occurrences site-wide). Rela's native `Apartment` block carries
  `@id: "https://eastlakeview503.relahq.com#listing"`, but the building node (`ApartmentComplex`)
  still has **no `@id`** to point at, so the link cannot be made cleanly by reference. Reopens if Rela
  adds an `@id` to the `ApartmentComplex` block.

## Done

- **✅ October Search Console links reading — DONE 2026-10-12** (reading taken 2026-10-05 by Tier 3,
  `reports/IMPLEMENTATION-2026-10-05.md`; closed here on import). **External links Total 0. Top
  linking sites "No data". Internal links 0.** Out-of-band knowledge and a **read**, not a change to
  the site, so the Tier-1-certification rule does not apply. **This 0 is expected and needs no
  action** — the link went live 2026-09-28 and Google has not re-crawled the Coldwell Banker bio page
  yet; direct fetch confirms the link is live, so the real count is 1. Supersedes the stale 2026-09-26
  reading. Next reading due the first run of November.

- **✅ First inbound link to the listing — DONE 2026-09-28, CONFIRMED LIVE BY TIER 1 2026-10-05,
  RE-CONFIRMED 2026-10-12.** Rank-1 target in `link_targets`, carried 3 weeks, closed. Path taken
  (per `reports/IMPLEMENTATION-2026-09-28-run2.md`): the broker admin's **Featured Listing** control
  only links CB's own listing page, so the owner used **My Website → About Me → Edit** and pasted this
  queue's drafted copy block with the first line linked. Verified by direct fetch: one
  `<a href="https://eastlakeview503.relahq.com/">` in server-rendered HTML, anchor text
  "1550 Eastlake Ave E #503—Riva Condominium, Seattle.", **no `rel="nofollow"`**, HTTP 200. Recorded
  in `state/last-snapshot.json` (`inbound_links.external_links_observed = 1`).
  **Note on measurement:** the weekly automated `mention_query` still does **not** surface this link
  and reports `third_party_count: 0`. Known blindness of that tool on this domain, not a
  contradiction. Treat the automated number as a floor.

- **✅ Agent name spelling settled — DONE 2026-09-26.** Coldwell Banker Danforth broker admin reads
  First `Omar` / Last `Senghore`; `Senghor` on the listing was a typo in one Rela field. Applied by
  Tier 3, independently confirmed live by Tier 1 the same day and re-confirmed 2026-10-12: 0 sitewide
  occurrences of "Senghor", all occurrences read "Senghore".

- **✅ Agent identity reconciled across sites — DONE 2026-09-26.** The listing's agent email moved
  from `change-re@outlook.com` (the Rela account login address leaking into the agent field) to the
  address on the owner's brokerage record, in all 3 places. The injected `RealEstateAgent` block
  gained `@id` (`https://omar-senghore.cbdanforth.com` — the exact `@id` the bio site publishes for
  itself), `jobTitle`, `image`, NWMLS `identifier` `NWM62208`, `areaServed` and `sameAs`. GA4 tag
  `G-95JF0FLSZH` verified still loading afterwards. Effect: the listing and the brokerage site now
  describe one person rather than two — which is exactly what makes the About Me link land on a
  matching entity.

- **✅ `RealEstateAgent` structured-data block — DONE 2026-09-18**, enriched 2026-09-26. Confirmed
  live by Tier 1 on both dates and again 2026-10-12. The page serves three structured-data payloads.

- **✅ First Search Console "Links" reading — DONE 2026-09-26.** External links 0, all "Top …" panels
  "No data". Superseded by the 2026-10-05 reading above; kept for the dated record.

## Closed / cut

- **✅ Search Console indexation — ANSWERED, stop asking.** Settled 2026-09-16: GSC showed "URL is on
  Google", Page indexing "Page is indexed", Indexing → Pages **Indexed = 1, Not indexed = 0**.
  Recorded in `state/last-snapshot.json` (`indexed: "yes (GSC 2026-09-16)"`). **Do not re-open this on
  the strength of a WebSearch miss.** Per the 2026-09-18 scope change Tier 1 no longer runs the
  verbatim-phrase check at all.

- **✂️ Photo alt text — CUT, platform-blocked, confirmed.** Settled 2026-09-18 inside the Rela Photo
  Gallery editor: the only per-photo field is **Description** and it does not emit an `alt` attribute.
  All 19 gallery images still render `alt=""`. **There is no alt-text field to find.** It lives on the
  Rela support chase and nowhere else.

- **✅ Baseline page speed — CLOSED, check disabled.** `pagespeed_skip: true` in
  `state/competitors.json` since 2026-09-18. Core Web Vitals here are entirely Rela-controlled, so the
  number would be unactionable even if we had it.

- **✅ README Slack channel name — already fixed.** `README.md` says `#all-seo-eastlake`
  (`C0C0X36DRBQ`).

- **✂️ Tracked query "Eastlake condo for sale Lake Union view" — RETIRED.** Unwinnable head term for
  a zero-authority orphan page.

- **ℹ️ Third-party sites showing $698,000 — not ours to chase.** First seen on a Redfin summary, and
  again 2026-10-12 on `exprealty.com` (still #1 for "1550 Eastlake Ave E #503"). Our own price is
  confirmed live at $649,888 every run. Aggregator figures are unwinnable and off-strategy. Do not
  re-raise.

- **ℹ️ Email signature and LinkedIn "Featured" links — NOT link targets.** No crawler sees an email
  signature; LinkedIn Featured links are nofollow and client-rendered. Never counted toward the link
  goal. See `state/competitors.json` → `link_targets.explicitly_not_link_targets`.

- **ℹ️ New `og:image:url` / `og:image:secure_url` tags (appeared 2026-09-26) — no action.** Both
  duplicate the existing `og:image`. Platform-side, cosmetic, harmless.

- **ℹ️ Tracked-query result-set volatility — observed, not actioned.** 2026-10-05 saw all four queries
  shift substantially, with `wicklundre.com` and `github.com` (our own repo) vanishing. 2026-10-12:
  three of four returned identical top-5 sets, and "eastlakeview503" gained two unrelated geographic
  results (a New York city-government site and a Wikipedia article on a Saskatoon neighbourhood). This
  is search-tool noise on a one-link page, not a competitive event. Record movement; do not re-plan
  on it.

- **ℹ️ compass.com structured-data expansion (2026-10-12) — no action.** The off-market Compass page
  for unit #203 went from 11 JSON-LD types to 14 (added `Product`, `RealEstateListing`,
  `SingleFamilyResidence`); same title, same MLS#, still off-market, still outranking us. A
  platform-wide schema change at Compass, not a move aimed at this building, and our own structured
  data is already richer and more specific. It only reinforces the standing point: an off-market page
  outranks ours, and that is an authority gap, not a markup gap.

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the
2026-09-10 through 2026-09-28 work (SEO & Social fields, property description rewrite, year built
1997, amenities 7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent`
JSON-LD, agent identity reconciliation, first inbound link).
