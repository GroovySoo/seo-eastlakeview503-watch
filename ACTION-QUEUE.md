# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do. Tier 2 rewrites this file each week. Top section = do now.

> **Rewritten by Tier 2, 2026-10-05.** Status changes below come from Tier 1's ACTION VERIFICATION
> section in `reports/EVIDENCE-2026-10-05.md` (live-page observation), not from assumption. Also folds
> in out-of-band knowledge from `reports/IMPLEMENTATION-2026-09-28.md` and
> `reports/IMPLEMENTATION-2026-09-28-run2.md`: the "Featured Listing" route in the Coldwell Banker
> broker admin links to CB's **own** listing page, not to the Rela site, so the link was made via
> **My Website → About Me** instead; and the CB listing card for MLS #2556157 does **not** currently
> point at the Rela site, which is where item 1 below comes from.

## ⭐ Milestone: the first inbound link is live

`https://omar-senghore.cbdanforth.com/` now carries
`<a href="https://eastlakeview503.relahq.com/">1550 Eastlake Ave E #503 — Riva Condominium, Seattle.</a>`
in its About Me section — **followed**, no `rel="nofollow"`, server-rendered, verified by Tier 1 on
2026-10-05. External links: **0 → 1**. Six weeks of "nothing on the web points at this page" is over.

Caveat kept honest: the weekly automated mention search still reports **0** (it has never been able
to see this domain), and the last Search Console reading (**0**, 2026-09-26) predates the link by nine
days. The real count is 1; the next GSC reading is action 2 below.

## Do now

_(week of 2026-10-05 — all on-page work is finished. Everything below is off-page. Two items, not
three: see the note under item 3.)_

### 1. Add the listing site as the "Virtual Tour" link on your Coldwell Banker listing (~3 minutes) — **highest value item on this list**

This repeats the move that just worked, in an admin you have now proven you can navigate. Your CB
listing page for #503 links to Coldwell Banker's own detail page but not to your site. The Virtual
Tour field is the standard place to fix that, and it is inbound link **#2** from the same strong
real-estate domain.

Click path:

1. Sign in to the Coldwell Banker Danforth agent portal.
2. **My Website → Listings**, find the card for **MLS #2556157**.
3. Open it for editing and look for a field labelled **Virtual Tour**, **Virtual Tour URL**,
   **Tour Link** or **Property Website**.
4. Paste exactly this into that field, and save:

```
https://eastlakeview503.relahq.com/
```

Reply in Slack with **"virtual tour done"** so Tier 1 can confirm it live next run.

**Escape hatch:** if there is no such field on the listing card, reply **"no virtual tour field"**.
That is a useful answer — it closes the item instead of carrying it.

### 2. Read your Search Console links number (~2 minutes) — **the monthly measurement, due this month**

This is the authoritative inbound-link count, and this month it tells us whether Google has noticed
the new link yet.

1. Go to **https://search.google.com/search-console** and sign in.
2. Pick the property **https://eastlakeview503.relahq.com/**.
3. In the left menu, click **Links**.
4. Read the box headed **Top linking sites**, and the **External links / Total** figure.

Reply in Slack with just the number and any site names listed, e.g.
**"GSC links: 1, omar-senghore.cbdanforth.com"** or **"GSC links: 0, No data"**.

Either answer is fine. A **0** this soon means only that Google has not recrawled the bio page yet —
it is not a sign that anything is wrong, and we will ask again next month.

### 3. Email Coldwell Banker Danforth marketing / the managing broker — fully drafted (3 minutes) *(carried 4 weeks)*

**Carried four weeks, so the ask is smaller this time.** The likeliest reason this keeps sliding is
that you do not have the right recipient. If that is it, reply in Slack with
**"brokerage contact: <name or email>"** — or **"don't know who to email"** — and we route around it
next week. That reply alone counts as doing this item.

If you do know who to send it to, it is a copy-paste. Supporting argument, unchanged:
`coldwellbankerhomes.com` — Coldwell Banker's own national site — ranks for "Riva Condominium Seattle
for sale" while this listing does not. The brand family already ranks for this building.

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

> **Why only three items, and why urbnlivn is not one of them.** In four weeks the owner completed
> exactly one item out of three — and it was the one that had been cut down to stand *alone*, with a
> fallback and an escape hatch. That is the format that works. Cold outreach to a blog is the hardest
> item on the list, so it waits its turn in "Next up" rather than being pasted here a fifth time.

## Next up (not this week)

- **Email urbnlivn.com — fully drafted (3 minutes)** *(carried 4 weeks; moved out of "Do now"
  2026-10-05 for list discipline, not because the target got worse)*. Rank 3 in
  `state/competitors.json` → `link_targets`, on the merits: a Seattle condo blog that covers Riva.
  **Deliberately not re-ranked on search movement again** — 2026-09-26 downgraded it because it left
  the tracked queries, 2026-09-28 upgraded it because it came back, and 2026-10-05 it has vanished
  from all four again, alongside `wicklundre.com` and our own monitoring repo. The tracked-query tool
  is too volatile on this domain to rank targets by. Promote this to "Do now" when item 1 or item 3
  above is spent. Use their site contact form or tips address.

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

  Reply in Slack with **"urbnlivn emailed"**. Next target after this one: the **Eastlake Community
  Council** (`https://www.eastlakeseattle.org/`, `link_targets` rank 4).

- **Add your WA real-estate licence number** (~2 minutes, two places). Empty in the Coldwell Banker
  broker admin (`Lic #`) and empty in Rela (`field_agent_bre`); marked "skip for now" by the owner on
  2026-09-26. It is public record and it is the strongest remaining trust signal for an agent entity
  now that the name, email and NWMLS ID all line up. Small but genuinely cheap.
- **Fill in the social-profile fields in the Coldwell Banker broker admin.** They are all blank, which
  is why the bio site's own `sameAs` array publishes five empty strings. Small effect, low effort.
- **Make the phone number format consistent.** Rela's native block emits `206-683-5030`; the injected
  agent block emits `+1-206-683-5030`. Both correct, one is not E.164. A two-character Tier 3 edit.
  Not worth a dedicated run.
- **Tier 3 browser reliability (maintainer task, not the owner's).** `playwright` MCP timed out on
  2026-09-26; Claude in Chrome disconnected mid-session on 2026-09-28 (and clicking "My Website" by
  mouse coordinates signed the owner out twice — the element's own JS `click()` worked instead).
  Each run has only succeeded because the other browser happened to work, or because the owner drove
  it by hand. Pick one browser and make it the reliable one; record the JS-click workaround.

## Backlog / blocked

- **Chase Rela support (the 8-item bundle) — IN BACKLOG since 2026-09-26** *(was carried 5 weeks)*.
  **Do not re-list it in "Do now".** Every item in it is cosmetic or entirely platform-controlled, and
  none of them is why this page doesn't rank. All 8 re-confirmed still outstanding on the live page
  2026-10-05, unchanged. The message is preserved and can be sent at any time in one paste:

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
  Confirmed absent again 2026-10-05 (0 occurrences site-wide). Rela's native `Apartment` block carries
  `@id: "https://eastlakeview503.relahq.com#listing"`, but the building node (`ApartmentComplex`)
  still has **no `@id`** to point at, so the link cannot be made cleanly by reference. Reopens if Rela
  adds an `@id` to the `ApartmentComplex` block.

## Done

- **✅ First inbound link to the listing — DONE 2026-09-28, CONFIRMED LIVE BY TIER 1 2026-10-05.**
  Rank-1 target in `link_targets`, carried 3 weeks, now closed. Path taken (per
  `reports/IMPLEMENTATION-2026-09-28-run2.md`): the broker admin's **Featured Listing** control only
  links CB's own listing page, so the owner used **My Website → About Me → Edit** and pasted this
  queue's drafted copy block with the first line linked. Tier 1 verified by direct fetch on 2026-10-05:
  one `<a href="https://eastlakeview503.relahq.com/">` in server-rendered HTML, anchor text
  "1550 Eastlake Ave E #503—Riva Condominium, Seattle.", **no `rel="nofollow"`**, HTTP 200. Prior runs
  through 2026-09-28 found 0 mentions. Recorded in `state/last-snapshot.json`
  (`inbound_links.external_links_observed = 1`).
  **Note on measurement:** the weekly automated `mention_query` did **not** surface this link and
  still reports `third_party_count: 0`. That is the known blindness of that tool on this domain, not a
  contradiction. Treat the automated number as a floor.

- **✅ Search Console "Links" number read — DONE 2026-09-26, the first verified inbound-link count.**
  Out-of-band knowledge from `reports/IMPLEMENTATION-2026-09-26-run2.md`; a **read**, not a change to
  the site, so the Tier-1-certification rule does not apply. **External links total 0. Top linking
  sites: No data. Top linking text: No data. Internal links: 0.** That reading is now **stale by
  design** — it predates the 2026-09-28 link by nine days. The monthly re-ask is "Do now" item 2.

- **✅ Agent name spelling settled — DONE 2026-09-26.** Coldwell Banker Danforth broker admin reads
  First `Omar` / Last `Senghore`; `Senghor` on the listing was a typo in one Rela field. Applied by
  Tier 3, independently confirmed live by Tier 1 the same day and re-confirmed 2026-10-05: 0 sitewide
  occurrences of "Senghor", all occurrences read "Senghore".

- **✅ Agent identity reconciled across sites — DONE 2026-09-26.** The listing's agent email moved
  from `change-re@outlook.com` (the Rela account login address leaking into the agent field) to the
  address on the owner's brokerage record, in all 3 places. The injected `RealEstateAgent` block
  gained `@id` (`https://omar-senghore.cbdanforth.com` — the exact `@id` the bio site publishes for
  itself), `jobTitle`, `image`, NWMLS `identifier` `NWM62208`, `areaServed` and `sameAs`. GA4 tag
  `G-95JF0FLSZH` verified still loading afterwards. Effect: the listing and the brokerage site now
  describe one person rather than two — which is exactly what makes the new About Me link land on a
  matching entity.

- **✅ `RealEstateAgent` structured-data block — DONE 2026-09-18**, enriched 2026-09-26. Confirmed
  live by Tier 1 on both dates and again 2026-10-05. The page serves three structured-data payloads.

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

- **✅ GA4 native-field item — CLOSED** (plan-locked; outcome achieved via Custom Script,
  `G-95JF0FLSZH` confirmed loading).

- **ℹ️ Third-party sites showing $698,000 — not ours to chase.** First seen on a Redfin summary, and
  again 2026-10-05 on `exprealty.com` (now #1 for "1550 Eastlake Ave E #503"). Our own price is
  confirmed live at $649,888 every run. Aggregator figures are unwinnable and off-strategy. Do not
  re-raise.

- **ℹ️ Email signature and LinkedIn "Featured" links — NOT link targets.** No crawler sees an email
  signature; LinkedIn Featured links are nofollow and client-rendered. Never counted toward the link
  goal. See `state/competitors.json` → `link_targets.explicitly_not_link_targets`.

- **ℹ️ New `og:image:url` / `og:image:secure_url` tags (appeared 2026-09-26) — no action.** Both
  duplicate the existing `og:image`. Platform-side, cosmetic, harmless.

- **ℹ️ Tracked-query result-set volatility — observed, not actioned.** On 2026-10-05 all four tracked
  queries returned substantially different domain sets, with `wicklundre.com` (top-2 every prior run)
  and `github.com` (our own repo, top result for the brand token every prior run) both vanishing, and
  "Riva Condos #503 Seattle" returning mostly Florida buildings. This is search-tool noise on a
  zero-to-one-link page, not a competitive event. Record movement; do not re-plan on it.

## Historical "Done" log

See `reports/STRATEGY-*.md` and `reports/IMPLEMENTATION-*.md` for the dated record of the
2026-09-10 through 2026-09-28 work (SEO & Social fields, property description rewrite, year built
1997, amenities 7→12, `ApartmentComplex` JSON-LD, GA4, `twitter:image:alt`, `RealEstateAgent`
JSON-LD, agent identity reconciliation, first inbound link).
