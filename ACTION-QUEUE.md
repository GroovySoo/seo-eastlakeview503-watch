# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-11-16.** Live-page status changes come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-11-16.md`, not from assumption. **No new Tier 3 implementation report
> since the last rewrite** (newest is still `reports/IMPLEMENTATION-2026-10-05.md`, folded in on
> 2026-10-12), so there is no new out-of-band knowledge to import. **The page is unchanged for a seventh
> consecutive week** — a mechanical field-by-field diff found zero substantive changes, so no on-page work
> is added. Three changes on Tier 2's own judgement, argued in `reports/STRATEGY-2026-11-16.md`:
> **(1) the ranked `link_targets` list is RESTOCKED** — the maintainer task escalated last week is done,
> and it produced one genuinely new free target with a verified editorial address, *The Registry*
> (`news.theregistryps.com`), which becomes "Do now" item 1; **(2) the Coldwell Banker "Virtual Tour" item
> reached the hard 2026-11-16 review date set for it last week and is retired to "## Backlog / blocked"**
> with its draft intact; **(3) `compass.com` is moved to `deep_fetch_dormant`** after a second consecutive
> bot-mitigated fetch failure, which was the trigger condition written into this file last week.
> Standing blocker unchanged: the Coldwell Banker broker admin is signed out. Settled fact carried forward:
> the CB listing-detail page for MLS #2556157 is not publicly discoverable, which is part of why item 1 of
> last week's list could never be certified from the page and has now been parked.

## ⭐ Milestone: the first inbound link is live and holding — seven weeks

`https://omar-senghore.cbdanforth.com/` carries
`<a href="https://eastlakeview503.relahq.com/">1550 Eastlake Ave E #503 — Riva Condominium, Seattle.</a>`
in its About Me section — **followed**, no `rel="nofollow"`, server-rendered. Verified by Tier 1 on
2026-10-05 and **re-verified byte-identical on 2026-10-12, 2026-10-19, 2026-10-26, 2026-11-02, 2026-11-09
and 2026-11-16** — seven consecutive weeks holding. External links: **0 → 1**.

Three measures still disagree, and all three stay recorded rather than collapsing into the flattering one:

| Measure | Reading | Worth |
|---|---|---|
| Tier 1 direct fetch | **1** | Authoritative. Re-confirmed 2026-11-16. |
| Weekly automated mention search | 0 | A floor. Has never been able to see this domain. |
| Search Console → Links (2026-10-05) | 0 | Real but lagging — Google had not re-crawled the bio page. |

**One link is still one link, and inbound links remain the single biggest lever on this listing.** The
Search Console reading that would settle the real count was asked for on 2026-11-02 and is **still
unanswered after two weeks** — it is "Do now" item 2 below.

## Do now

_(week of 2026-11-16 — all on-page work is finished; everything below is off-page. The page has now been
byte-for-byte unchanged for seven consecutive weeks, which is the correct state.)_

### 1. Email *The Registry* about the building (~3 minutes) — **NEW this week, and the best free link ask on the list**

*The Registry* is a Pacific Northwest real-estate news publication. It is the one target on our whole
list that is free, reachable, topically perfect **and has never been tried**. It is also a completely
different *kind* of site from the brokerage pages that make up the rest of our link profile, which is
exactly what a profile holding one link needs.

- **Send to: `letters@theregistryps.com`** — the editorial address published on
  `https://news.theregistryps.com/contact/` (HTTP 200, verified 2026-11-16).

**Paste this, change nothing but your own sign-off if you want to:**

> Subject: Riva Condominium (1550 Eastlake Ave E) — top-floor unit on the market in Eastlake
>
> Hi — I'm a Coldwell Banker Danforth broker working in Eastlake, and I'm handling the sale of a
> top-floor unit at Riva Condominium, 1550 Eastlake Ave E. It's a 1997 building, five floors, 2 bed /
> 2 bath, 1,114 sq ft, with Lake Union and skyline views from a private balcony, two secured parking
> spaces and storage. Listed at $649,888 (MLS# 2556157).
>
> If you're tracking Eastlake or Lake Union condo activity, I'm glad to be a source on this one —
> happy to share what we're seeing on pricing, days on market and the kind of buyer looking at
> smaller Eastlake buildings right now. Full details, photos and floor information are here:
> https://eastlakeview503.relahq.com/
>
> Omar Senghore, Coldwell Banker Danforth (Everett) — 206-683-5030

**Why it is written that way:** it pitches **the building and the local market**, and it offers to be a
source. It does **not** ask for a link. Editorial outlets decline link requests as a matter of course; a
useful local data point is what actually gets used — and a mention that gets used carries the link.

Reply **"registry emailed"** when it has gone, or **"registry declined"** if they come back with a no.
Either answer is worth having.

### 2. Read your Search Console "Top linking sites" number (~2 minutes) *(carried 2 weeks)*

This is the authoritative reading of the one thing that matters most. It was asked for on 2026-11-02 and
no answer has come back, so it carries — it is **not** being re-asked as a new monthly task, and the next
scheduled monthly ask is the first week of December.

1. Go to `https://search.google.com/search-console` and sign in.
2. Pick the property for **eastlakeview503.relahq.com**.
3. In the left menu click **Links**.
4. Look at the box headed **Top linking sites**.

Reply in Slack with the **"External links / Total"** number and any site names listed — even if it still
says **"No data"**, that is a real answer and worth sending. Expected: `omar-senghore.cbdanforth.com`,
total 1.

### 3. Add your site to the "Website" field on your Zillow and Realtor.com agent profiles (~5 minutes each) *(carried 3 weeks)*

Rank 5 in `state/competitors.json` → `link_targets`. Owner-controlled, no login you are stuck on.

- Zillow: `https://www.zillow.com/agent-profile/` → sign in → **Edit profile**.
- Realtor.com: `https://www.realtor.com/realestateagents/` → claim/sign in → **Edit**.

On each profile find the field labelled **Website**, **Personal website** or **My website** and paste:

```
https://eastlakeview503.relahq.com/
```

Reply **"profiles updated"**.

**Read this before you count it as a win:** both of those fields are `nofollow`. They pass **no ranking
credit** and **must never be counted toward the link goal** — your confirmed link count stays at **1**
after doing this. What they give you is free referral traffic from exactly the right audience. That is a
traffic win, not an SEO one, and it is still worth ten minutes.

**Carried-3-weeks note (2026-11-16).** Called out as required. This item is not blocked and not too hard —
it is simply unglamorous. But it is traffic-only, so it will **not** keep holding a "Do now" slot ahead of
real link work: **if it has not moved by 2026-11-23 it drops to "## Next up"**, not to Backlog, because it
stays genuinely easy to do whenever you feel like it.


## Next up (not this week)

- **✅ RESOLVED 2026-11-16 — `link_targets` restocked.** The maintainer task escalated on 2026-11-09 is
  done. Eight candidate domains were checked live with a browser UA; `state/competitors.json` →
  `link_targets` now has **8 ranked targets, a `draw_order`, and a `rejected_candidates` list**. The one
  genuinely new free target with a verified editorial address — *The Registry*, `letters@theregistryps.com`
  — is "Do now" item 1 above. Two paid directory options (Seattle Metro Chamber, GSBA) are listed at
  ranks 7–8 and **ranked last on purpose: do not spend money on them**, because this microsite is a
  temporary asset that disappears when the condo sells. Four candidates were excluded for cause and the
  reasons are recorded so nobody re-proposes them — notably **`lakeunionbeat.com`, which is still cited as
  an Eastlake news source by a City of Seattle document but has been dropped and re-registered as gambling
  spam**; a link from it would now be actively harmful. **Read the real finding, though:** ranks 3 and 4
  (urbnlivn, Eastlake Community Council) are free, take one email each, and had their recipients
  **re-verified live on 2026-11-16** — they sit in Backlog only because the email was never sent. The
  constraint on the #1 lever is no longer a shortage of targets. One domain, `sluchamber.org`, is
  geographically the best-fitting chamber (the listing is a block from South Lake Union) but did not
  respond at all today; worth one re-check at the next restock, not before.
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
- **✅ RESOLVED 2026-11-16 — `compass.com` moved to `deep_fetch_dormant`.** It returned the same
  bot-mitigated **HTTP 202 with an empty body** for a **second consecutive week** (both the `/listing/`
  redirect and the final `/homedetails/` URL, after one retry), which is exactly the trigger condition
  written into this file on 2026-11-09. Tier 1 flagged it and left the call to Tier 2; the call is made.
  Its URL and redirect target are unchanged across every run, so this is bot mitigation, **not a page
  change** — its title/meta (2026-11-02) and JSON-LD types (2026-10-19) stay carried forward in
  `state/last-snapshot.json` **with provenance, not nulled**. This stops burning a retry every run. The
  strategic value of the finding is already banked and unchanged: an **off-market** page on a
  high-authority domain still outranks our live listing while carrying no listing structured data — the
  cleanest proof we have that this race is decided by domain authority, not on-page work. Reinstate it to
  `deep_fetch` if it ever returns a body again. `windermere.com` is now the only weekly deep fetch.

## Backlog / blocked

- **Paste your site into the "Virtual Tour" field on your Coldwell Banker listing — RETIRED TO BACKLOG
  2026-11-16** *(was carried 5 weeks in "Do now"; a sixth listing would have been due today)*. **Do not
  re-list it in "Do now".** On 2026-11-09 this item was promoted to #1 and given an explicit review date of
  **2026-11-16**, with the rule stated in writing: if nothing had moved by then it goes to Backlog. That
  date is today and Tier 1 reports no movement, so the rule is applied to it exactly as it was applied to
  the urbnlivn, brokerage and Eastlake Community Council asks. **Being honest about why:** this item is
  **not blocked and not too hard** — four steps, about three minutes, on a site the owner has an account
  for. It is parked purely because it has not been done. There is also a structural reason it could never
  resolve itself: **Tier 1 can never verify it from the page** (see the settled fact below), so it only
  ever closes on the owner's word, and an item that can only close on a word nobody says does not belong at
  the top of the list for a sixth week. **It is still worth doing** — it would be inbound link **#2** from
  the same strong real-estate domain that gave us link #1, which is more than any other open item can
  claim. It reopens instantly: reply **"virtual tour added"** and Tier 1 will start re-checking it, or
  **"no virtual tour field"** and it closes for good. Everything needed is preserved here:

  1. Go to `https://www.cbdanforth.com/`, click **Broker Login**, and sign in.
  2. **My Website → Listings**, find the card for **MLS #2556157**.
  3. Open it for editing and look for a field labelled **Virtual Tour**, **Virtual Tour URL**, **Tour Link**
     or **Property Website**.
  4. Paste exactly this into that field, and save:

  ```
  https://eastlakeview503.relahq.com/
  ```

  **Settled, so nobody re-checks it:** the Coldwell Banker *listing* page for MLS #2556157 is not visible
  anywhere on the public web (`/listing/2556157` and `/Listing/2556157` on both the bio subdomain and
  `www.cbdanforth.com` return 404; the IDX search path loads but renders its results in the browser, so
  there is nothing for an automated check to read). **This is why the weekly check can never confirm this
  item**, and why "no virtual tour field" is just as valuable an answer as doing it.

- **Email the Eastlake Community Council — RETIRED TO BACKLOG 2026-11-09** *(was carried 4 weeks in "Do
  now")*. **Do not re-list it in "Do now".** On 2026-11-02 this item was given one more week with an
  explicit hard deadline of **2026-11-09**; that deadline is today, Tier 1 reports no evidence either way,
  and under the rule as written that means not moved. Same treatment as the urbnlivn and brokerage emails.
  **Being honest about why:** this item is **not blocked and not too hard** — the address is verified, the
  email is written out below, it needs no login and takes about three minutes. It is parked purely because
  it has not been sent, and keeping an un-sent three-minute task at the top of the list for a fifth week
  costs the list more credibility than the item is worth. **It is still worth doing**, it was rank 4 on the
  merits, and it reopens instantly — reply **"ECC emailed"** or **"ECC declined"**. Everything needed is
  preserved here:

  - **Send to: `info@eastlakeseattle.org`** — published on `https://www.eastlakeseattle.org/` (HTTP 200,
    verified 2026-10-19).
  - **Why this target:** hyper-local, topically relevant neighbourhood domain, and an entirely different
    *kind* of domain from the real-estate sites — which is what a link profile holding exactly one link
    needs.
  - **Framing note:** this is a neighbourhood-interest and local-business ask, **not** a link request. Do
    not rewrite it into "please link to my site" — community sites decline those, and the offer of help is
    the part that actually opens the door.

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

  **Note for the maintainer:** retiring this empties the ranked `link_targets` list — see the escalated
  restock task in "## Next up".

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

- **✅ First inbound link to the listing — DONE 2026-09-28, CONFIRMED LIVE BY TIER 1 2026-10-05, and
  RE-CONFIRMED BYTE-IDENTICAL EVERY WEEK SINCE, THROUGH 2026-11-16 — seven consecutive weeks.** Rank-1 target in `link_targets`, carried 3 weeks,
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
