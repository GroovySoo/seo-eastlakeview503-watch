# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-10-26.** Live-page status changes come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-10-26.md`, not from assumption. **No new Tier 3 implementation report
> since the last rewrite** (newest is still `reports/IMPLEMENTATION-2026-10-05.md`, folded in on
> 2026-10-12), so there is no new out-of-band knowledge to import. Three changes on Tier 2's own
> judgement, all argued in `reports/STRATEGY-2026-10-26.md`: the **urbnlivn.com email is retired to
> Backlog** at 7 weeks under the same rule that parked the brokerage email at 5; the **Zillow /
> Realtor.com profile item is promoted** into the freed slot; and **item 5 of the Rela support chase is
> narrowed from three missing social tags to two**, because `og:url` appeared on the live page this run.
> Standing blocker unchanged: the Coldwell Banker broker admin is signed out. **New settled fact:** the
> CB listing-detail page for MLS #2556157 is not publicly discoverable, so Tier 1 can never certify
> "Do now" item 1 from the page — it closes on the owner's word or not at all.

## ⭐ Milestone: the first inbound link is live and holding — four weeks

`https://omar-senghore.cbdanforth.com/` carries
`<a href="https://eastlakeview503.relahq.com/">1550 Eastlake Ave E #503 — Riva Condominium, Seattle.</a>`
in its About Me section — **followed**, no `rel="nofollow"`, server-rendered. Verified by Tier 1 on
2026-10-05 and **re-verified byte-identical on 2026-10-12, 2026-10-19 and 2026-10-26** — four consecutive
weeks holding, and independently re-confirmed by Tier 2 this run. External links: **0 → 1**.

Three measures still disagree, and all three stay recorded rather than collapsing into the flattering one:

| Measure | Reading | Worth |
|---|---|---|
| Tier 1 direct fetch | **1** | Authoritative. Re-confirmed 2026-10-26. |
| Weekly automated mention search | 0 | A floor. Has never been able to see this domain. |
| Search Console → Links (2026-10-05) | 0 | Real but lagging — Google had not re-crawled the bio page. |

**A Search Console 0 at that stage was not a problem and needed no action.** The next reading is due
**2026-11-02** and is the first one that will mean anything.

## Do now

_(week of 2026-10-26 — all on-page work is finished; everything below is off-page. The page has now been
byte-for-byte unchanged for four consecutive weeks apart from one benign platform-side tag addition,
which is the correct state.)_

### 1. Paste your site into the "Virtual Tour" field on your Coldwell Banker listing (~3 minutes) — **highest value item on this list** *(carried 3 weeks)*

This is inbound link **#2** from the same strong real-estate domain that gave us link #1.

1. Go to `https://www.cbdanforth.com/`, click **Broker Login**, and sign in.
2. **My Website → Listings**, find the card for **MLS #2556157**.
3. Open it for editing and look for a field labelled **Virtual Tour**, **Virtual Tour URL**, **Tour Link**
   or **Property Website**.
4. Paste exactly this into that field, and save:

```
https://eastlakeview503.relahq.com/
```

**If there is no such field on the card, that answer is just as valuable as doing it** — reply
**"no virtual tour field"** and this closes for good instead of carrying another week.

**Carried-3-weeks note (2026-10-26).** Kept rather than retired because it is the highest-value item on
the list and you have already done one comparable self-service job in this same portal — the About Me
edit that produced your first link. What changed this week is that the ask is cut back to the four steps
above only. The "just sign in and we'll do it Monday" option is still available, but it is no longer the
headline: it can only reach us as a Slack reply, and no weekly ask has been replied to yet, so it is not a
route this item can realistically close through. **Next review 2026-11-16** — if nothing has moved by
then it goes to Backlog.

**Also settled this week, so nobody re-checks it:** your Coldwell Banker *listing* page for MLS #2556157
is not visible anywhere on the public web (`/listing/2556157` and `/Listing/2556157` on both the bio
subdomain and `www.cbdanforth.com` return 404; the IDX search path loads but renders its results in the
browser, so there is nothing for an automated check to read). **This means the weekly check can never
confirm this item for you.** It closes when you tell us, either way.

### 2. Email the Eastlake Community Council — fully drafted, address looked up (~3 minutes) *(carried 2 weeks)*

Rank 4 in `state/competitors.json` → `link_targets`: a hyper-local, topically relevant neighbourhood
domain. Local-community links are exactly the kind a single-listing microsite can realistically earn, and
this is an entirely different *kind* of domain from the two real-estate sites — which is good for a link
profile that currently has exactly one link in it.

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

### 3. Add your site to the "website" field on your Zillow and Realtor.com agent profiles (~5 minutes each) *(promoted from "Next up" 2026-10-26)*

Rank 5 in `state/competitors.json` → `link_targets`. Promoted into the slot freed by retiring the
urbnlivn email. Chosen deliberately: it is **owner-controlled, needs no login you are currently stuck on,
and depends on nobody else's reply** — and the only two things that have ever actually shipped on this
project were owner-controlled self-service edits.

On each profile, find the field labelled **Website**, **Personal website** or **My website**, and paste:

```
https://eastlakeview503.relahq.com/
```

- Zillow: `https://www.zillow.com/agent-profile/` → sign in → **Edit profile**.
- Realtor.com: `https://www.realtor.com/realestateagents/` → claim/sign in to your profile → **Edit**.

**Be clear what this is and is not.** Both fields are `nofollow`, so they pass **no ranking credit** and
**must never be counted toward the link goal** — your link count stays at 1 after doing this. What they do
give you is **referral traffic from exactly the right audience**, free, from two of the highest-traffic
property sites in the US. That is worth five minutes on its own merits; it is not an SEO link.

Reply in Slack with **"profiles updated"**.

## Next up (not this week)

- **Research new link targets — maintainer task, not the owner's.** `state/competitors.json` →
  `link_targets` is nearly exhausted: rank 1 done, ranks 2 and 3 in Backlog, rank 4 is this week's ask,
  rank 5 is nofollow/traffic-only. Within two weeks there is no ranked target left to draw a weekly ask
  from, and the standing rule is to draw from the verified list rather than invent generic advice. Needs
  new **named, verified-live** targets (Seattle neighbourhood press, condo-building directories, local
  business and community sites), each checked for a real editorial path before it is listed.
- **Fill in the social-profile fields in the Coldwell Banker broker admin.** All blank, which is why the
  bio site's own `sameAs` array publishes five empty strings. Small effect, low effort.
- **Make the phone number format consistent.** Rela's native block emits `206-683-5030`; the injected
  agent block emits `+1-206-683-5030`. Both correct, one is not E.164. A two-character Tier 3 edit; not
  worth a dedicated run.
- **Tier 3 browser reliability (maintainer task).** Claude in Chrome worked cleanly on 2026-10-05 —
  connected first call, navigated and closed its tab — the third consecutive clean data point, after
  `playwright` MCP timed out 2026-09-26 and Chrome disconnected mid-session 2026-09-28. Standing
  workarounds to keep recorded: prefer an element's own JS `click()` over mouse coordinates in the CB
  admin (coordinates signed the owner out twice); `javascript_tool` is blocked whenever a returned value
  contains a URL with a query string, so return `{origin, pathname, hasQuery}` instead of a raw href;
  Search Console accepts a direct deep link to the Links report with the property pre-selected, which
  skips the property picker.

## Backlog / blocked

- **Email urbnlivn.com — RETIRED TO BACKLOG 2026-10-26** *(was carried 7 weeks in "Do now" — the oldest
  item on the project)*. **Do not re-list it in "Do now".** Same rule and same reasoning that parked the
  brokerage email at 5 weeks: it was cut down twice — a full paste-ready draft on 2026-09-18, then the
  recipient looked up and verified on 2026-10-19 — and moved neither time. An eighth listing would cost
  the weekly list more credibility than the item is worth. **It is still worth doing**, it is still rank 3
  on the merits, and it reopens the moment you say a word about it: reply **"urbnlivn emailed"** or
  **"urbnlivn declined"**. Everything needed is preserved here:

  - **Send to: `matt@urban-living.com`.** urbnlivn.com publishes `matt@`, `alicia@` and
    `land@urban-living.com` on its homepage. The blog is published by **Urban Living, a Seattle condo
    brokerage**, so these are the editorial side.
  - **Also paste it into the form at `https://www.urbnlivn.com/contact-us`** (HTTP 200, verified
    2026-10-19). Belt and braces; costs ten seconds.
  - **Confirmed on the merits:** their homepage mentions "Riva" **three times**. The building genuinely is
    on their beat — this was never a cold generic pitch.
  - **They are a competing brokerage, so the draft leads with the building, not with the listing.** That
    framing is deliberate. Do not rewrite it into a "please promote my listing" ask.

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

  **Do not re-rank this target on search movement.** 2026-09-26 downgraded it because it left the tracked
  queries, 2026-09-28 upgraded it because it came back, and it has been absent from all four since
  2026-10-05. The tracked-query tool is too volatile on this domain to rank targets by.

- **Add your Washington real-estate licence number — RETIRED TO BACKLOG 2026-10-19.** **Do not re-list it
  in "Do now".** The owner replied **"skip for now"** on 2026-09-26. It was re-raised once on 2026-10-12
  as a cheap trust signal, under an explicit once-only rule, and no reply came; Tier 1 re-confirmed on
  2026-10-26 that no licence number appears anywhere in the live page's agent data. **It is still worth
  doing** and reopens the moment the owner wants it — reply **"licence added"** and Tier 1 will confirm
  the Rela side on the live page next run. Two labelled fields, same number in both:

  1. Coldwell Banker Danforth broker admin → **My Website → Contact Info** → field marked **Lic #**.
  2. Rela editor → **Theme & Contacts** → field marked **field_agent_bre**.

- **Email Coldwell Banker Danforth marketing / the managing broker — MOVED TO BACKLOG 2026-10-12**
  *(was carried 5 weeks)*. **Do not re-list it in "Do now".** It was cut down twice — full draft, then
  "just name a recipient" — and moved neither time, which says the blocker is real and outside the
  owner's control: there is no known marketing contact at the brokerage and nothing on this list can
  manufacture one. It also aims at the same prize as "Do now" item 1 (a link on a Coldwell Banker domain)
  by a route that depends on a third party, where item 1 depends on nobody. Reopens the moment the owner
  learns a recipient — reply **"brokerage contact: <name or email>"** and it goes straight back to "Do
  now". Supporting argument, unchanged: `coldwellbankerhomes.com` ranks for "Riva Condominium Seattle for
  sale" while this listing does not. The draft is preserved:

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

- **Chase Rela support (now a 7½-item bundle) — IN BACKLOG since 2026-09-26.** **Do not re-list it in "Do
  now".** Every item in it is cosmetic or entirely platform-controlled, and none of them is why this page
  doesn't rank. **Item 5 was narrowed on 2026-10-26: `og:url` is now live on the page, so the ask is two
  tags, not three.** The other 7 re-confirmed still outstanding on the live page 2026-10-26. The message
  is preserved and can be sent at any time in one paste:

  > Hi — I run a single-property site on Rela (eastlakeview503.relahq.com) and there are a few
  > SEO items I can't reach from the editor. Could you get these in front of the product team?
  >
  > 1. `/sitemap.xml` returns 404 — there is no sitemap for the site.
  > 2. `robots.txt` has `Crawl-delay: 10` and no `Sitemap:` line.
  > 3. `/llms.txt` returns the normal page HTML instead of llms.txt content.
  > 4. No per-photo alt text: the Photo Gallery editor only has a Description field, and it doesn't
  >    become an `alt` attribute — all 19 listing photos render `alt=""`.
  > 5. Missing social tags: `og:locale` and `twitter:card`. (`og:url` arrived in late October — thank
  >    you — these two are still absent.)
  > 6. The H1 reads "1550 Eastlake Ave E Apt 503, Seattle" — I'd like "1550 Eastlake Ave E #503,
  >    Seattle, WA 98102".
  > 7. Listing structured data uses `numberOfRooms` rather than `numberOfBedrooms`, and has no
  >    `amenityFeature`, `petsAllowed` or `containedInPlace`.
  > 8. Listing photos have no `loading="lazy"`.
  >
  > Thanks — happy to give any detail you need.

- **Link the structured-data blocks (`containedInPlace`) — STILL BACKLOG** *(was carried 4 weeks)*.
  Confirmed absent again 2026-10-26 (0 occurrences site-wide). Rela's native `Apartment` block carries
  `@id: "https://eastlakeview503.relahq.com#listing"`, but the building node (`ApartmentComplex`) still
  has **no `@id`** to point at, so the link cannot be made cleanly by reference. Reopens if Rela adds an
  `@id` to the `ApartmentComplex` block.

## Done

- **✅ October Search Console links reading — DONE 2026-10-12** (reading taken 2026-10-05 by Tier 3,
  `reports/IMPLEMENTATION-2026-10-05.md`; closed here on import). **External links Total 0. Top linking
  sites "No data". Internal links 0.** Out-of-band knowledge and a **read**, not a change to the site, so
  the Tier-1-certification rule does not apply. **That 0 was expected and needed no action** — the link
  went live 2026-09-28 and Google had not re-crawled the Coldwell Banker bio page; direct fetch confirms
  the link is live, so the real count is 1. **Next reading due 2026-11-02**, the first run of November,
  and it is the first one that will be genuinely informative.

- **✅ First inbound link to the listing — DONE 2026-09-28, CONFIRMED LIVE BY TIER 1 2026-10-05,
  RE-CONFIRMED 2026-10-12, 2026-10-19 and 2026-10-26.** Rank-1 target in `link_targets`, carried 3 weeks,
  closed. Path taken (per `reports/IMPLEMENTATION-2026-09-28-run2.md`): the broker admin's **Featured
  Listing** control only links CB's own listing page, so the owner used **My Website → About Me → Edit**
  and pasted this queue's drafted copy block with the first line linked. Verified by direct fetch: one
  `<a href="https://eastlakeview503.relahq.com/">` in server-rendered HTML, anchor text "1550 Eastlake Ave
  E #503—Riva Condominium, Seattle.", **no `rel="nofollow"`**, HTTP 200. Recorded in
  `state/last-snapshot.json` (`inbound_links.external_links_observed = 1`).
  **Note on measurement:** the weekly automated `mention_query` still does **not** surface this link and
  reports `third_party_count: 0`. Known blindness of that tool on this domain, not a contradiction. Treat
  the automated number as a floor.

- **✅ Agent name spelling settled — DONE 2026-09-26.** Coldwell Banker Danforth broker admin reads First
  `Omar` / Last `Senghore`; `Senghor` on the listing was a typo in one Rela field. Applied by Tier 3,
  independently confirmed live by Tier 1 the same day and re-confirmed 2026-10-26: 0 sitewide occurrences
  of "Senghor", all occurrences read "Senghore".

- **✅ Agent identity reconciled across sites — DONE 2026-09-26.** The listing's agent email moved from
  `change-re@outlook.com` (the Rela account login address leaking into the agent field) to the address on
  the owner's brokerage record, in all 3 places. The injected `RealEstateAgent` block gained `@id`
  (`https://omar-senghore.cbdanforth.com` — the exact `@id` the bio site publishes for itself), `jobTitle`,
  `image`, NWMLS `identifier` `NWM62208`, `areaServed` and `sameAs`. GA4 tag `G-95JF0FLSZH` verified still
  loading afterwards. Effect: the listing and the brokerage site now describe one person rather than two —
  which is exactly what makes the About Me link land on a matching entity.

- **✅ `RealEstateAgent` structured-data block — DONE 2026-09-18**, enriched 2026-09-26. Confirmed live by
  Tier 1 on both dates and again 2026-10-26. The page serves three structured-data payloads.

- **✅ First Search Console "Links" reading — DONE 2026-09-26.** External links 0, all "Top …" panels "No
  data". Superseded by the 2026-10-05 reading above; kept for the dated record.

## Closed / cut

- **ℹ️ `og:url` appeared on the live page 2026-10-26 — no action, and good news.** Absent in every
  snapshot 2026-09-11 → 2026-10-19, now present as `https://eastlakeview503.relahq.com` (self-referencing,
  matching the canonical). Unasked and platform-side, but an **improvement, not a regression**:
  `og:updated_time` did not move, so Rela shipped it without touching listing content. Consequence already
  applied: item 5 of the Rela support chase above now asks for two tags instead of three.

- **✅ Whether a CB listing-detail page can be checked automatically — ANSWERED 2026-10-26, stop looking.**
  There is no publicly readable Coldwell Banker listing-detail page for MLS #2556157. `/listing/2556157`
  and `/Listing/2556157` on both `omar-senghore.cbdanforth.com` and `www.cbdanforth.com` → 404;
  `/mylistings/aid-991320` → 404; `/Search/Seattle/mls-2556157/aid-991320` → HTTP 200 but client-rendered,
  with zero occurrences of "1550 Eastlake" in the server HTML. The bio page carries "MLS# 2556157" only
  inside the About Me prose that already holds link #1. **Therefore "Do now" item 1 can never be certified
  from the page** and closes on the owner's word or not at all. Do not spend another run probing for it.

- **✅ Search Console indexation — ANSWERED, stop asking.** Settled 2026-09-16: GSC showed "URL is on
  Google", Page indexing "Page is indexed", Indexing → Pages **Indexed = 1, Not indexed = 0**. Recorded in
  `state/last-snapshot.json` (`indexed: "yes (GSC 2026-09-16)"`). **Do not re-open this on the strength of
  a WebSearch miss.** Per the 2026-09-18 scope change Tier 1 no longer runs the verbatim-phrase check.

- **✂️ Photo alt text — CUT, platform-blocked, confirmed.** Settled 2026-09-18 inside the Rela Photo
  Gallery editor: the only per-photo field is **Description** and it does not emit an `alt` attribute. All
  19 gallery images still render `alt=""`. **There is no alt-text field to find.** It lives on the Rela
  support chase and nowhere else.

- **✅ Baseline page speed — CLOSED, check disabled.** `pagespeed_skip: true` in
  `state/competitors.json` since 2026-09-18. Core Web Vitals here are entirely Rela-controlled, so the
  number would be unactionable even if we had it.

- **✅ README Slack channel name — already fixed.** `README.md` says `#all-seo-eastlake` (`C0C0X36DRBQ`).

- **✂️ Tracked query "Eastlake condo for sale Lake Union view" — RETIRED.** Unwinnable head term for a
  zero-authority orphan page.

- **ℹ️ Third-party sites showing $698,000 — not ours to chase.** First seen on a Redfin summary, and again
  2026-10-26 on `exprealty.com` (still #1 for "1550 Eastlake Ave E #503"). Our own price is confirmed live
  at $649,888 every run. Aggregator figures are unwinnable and off-strategy. Do not re-raise.

- **ℹ️ Email signature and LinkedIn "Featured" links — NOT link targets.** No crawler sees an email
  signature; LinkedIn Featured links are nofollow and client-rendered. Never counted toward the link goal.
  See `state/competitors.json` → `link_targets.explicitly_not_link_targets`. The same rule applies to the
  Zillow / Realtor.com profile fields in "Do now" item 3: those are referral traffic, not links.

- **ℹ️ New `og:image:url` / `og:image:secure_url` tags (appeared 2026-09-26) — no action.** Both duplicate
  the existing `og:image`. Platform-side, cosmetic, harmless.

- **ℹ️ Tracked-query result-set volatility — observed, not actioned.** 2026-10-05 saw all four queries
  shift substantially. 2026-10-12 and 2026-10-19 were near-identical. 2026-10-26: three of four identical,
  the fourth swapping one Florida "Riva" domain for another at rank 4. This is search-tool noise on a
  one-link page, not a competitive event. Record movement; do not re-plan on it.

- **ℹ️ compass.com structured-data expansion (2026-10-12) — no action.** The off-market Compass page for
  unit #203 went from 11 JSON-LD types to 14 (added `Product`, `RealEstateListing`,
  `SingleFamilyResidence`); same title, same MLS#, still off-market, still outranking us. A platform-wide
  schema change at Compass, not a move aimed at this building, and our own structured data is already
  richer and more specific. It only reinforces the standing point: an off-market page outranks ours, and
  that is an authority gap, not a markup gap.

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the 2026-09-10
through 2026-09-28 work (SEO & Social fields, property description rewrite, year built 1997, amenities
7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent` JSON-LD, agent identity
reconciliation, first inbound link).
