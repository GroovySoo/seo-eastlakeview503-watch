# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do for a browser session (Claude in Chrome, logged into Rela + Google).
Tier 2 rewrites this file each week. Top section = do now.

## Do now

_(week of 2026-09-16 — full copy/paste text in `reports/STRATEGY-2026-09-16.md` §2)_

**All three carried over. None were done last week, so all three have been cut down to ten minutes
each.** The longer versions are still in `STRATEGY-2026-09-14.md` §2 if a bigger session opens up.

1. **Put TWO links on the internet pointing at the page** (10 min) *(carried 2 weeks)*. The page
   still has **zero** external links — the single biggest lever available. Not seven placements
   this week, **two**: (a) email signature, (b) LinkedIn → Add profile section → Recommended →
   Add featured → Add a link. Link text both times:
   `1550 Eastlake Ave E #503 — Riva Condominium`, pointing at
   `https://eastlakeview503.relahq.com/`. Exact field-by-field text in memo §2.1. Reply in Slack
   with "signature done" / "LinkedIn done" so this can close.
2. **Settle the Search Console question, once** (10 min) *(carried 2 weeks)*. GSC → pick the
   `eastlakeview503.relahq.com` property → paste `https://eastlakeview503.relahq.com/` into the top
   search bar → Enter. Write down the exact headline ("URL is on Google" / "URL is not on Google" /
   "URL is available to Google"), click **Request Indexing** if it is not indexed, then open
   **Indexing → Pages** and note the "Not indexed" count and top reason. Report both in Slack.
   **This is verification, not an alarm** — nothing on the page blocks indexing, and GSC itself said
   indexed on 2026-09-10. This item closes after this week either way.
3. **Describe just the first FIVE photos** (10 min) *(carried 1 week)*. 0 of 19 property photos have
   alt text; the only 3 alt attributes on the page are on logos. Last week asked for all 19 and it
   did not happen — do five. Rela → listing → **Photos** → first photo → look for an **Alt text /
   Description / Caption** field → describe what is actually visible → save → repeat for photos 2–5.
   Five ready-to-adapt lines in memo §2.3 (vary them, do not paste one line five times).
   **If no such field exists**, it is platform-side: say so in Slack and it moves to the Rela
   support chase below.

**One-line ask, not a task (30 seconds):** reply in Slack with your **phone number** — it unblocks
the three-week-old agent-details item below.

## Next up (not this week)

- **Chase Rela on the sitemap + robots.txt** *(carried 2 weeks)*. `/sitemap.xml` still 404,
  `robots.txt` still `Crawl-delay: 10` with no `Sitemap:` line — Tier 1 confirms **NOT DONE**.
  Deliberately not its own Do-now slot: for a one-page site a sitemap is close to cosmetic and
  Google ignores `Crawl-delay`. Folded into the Rela support message if Do-now item 3 turns out to
  be platform-blocked.
- **Link the two JSON-LD nodes** *(carried 2 weeks)*. The unit (`Apartment`) and building
  (`ApartmentComplex`) nodes both exist but are not connected, so Google is not told that unit #503
  is inside Riva Condominium. Fix means adding `containedInPlace` in Rela → Advanced → Custom
  Script. Do it in the same editing pass as the agent-details item below, not on its own.

## Backlog / blocked

- **Inbound links** (owner) — promoted to "Do now" item 1. Still the **#1 ranking lever**: the page
  has zero external links pointing to it. An off-market Compass page for unit #203 outranks us on
  domain strength alone.
- **Extend the Custom-Script JSON-LD with a full `RealEstateAgent` node** — Tier 1 confirms **NOT
  DONE** again on 2026-09-16 *(carried 3 weeks)*. ⚠️ **Threshold crossed — rewritten smaller.**
  Genuinely blocked, not hard: neither agent can obtain the owner's own contact details. The ask is
  now **the phone number alone**; brokerage name and headshot URL are dropped from the immediate
  ask. The only agent data on the page is still `name` + `email` (`Omar Senghor`,
  `change-re@outlook.com`) on the `Apartment` node's `provider`. **If the phone number is not
  supplied by 2026-09-21, this item is cut**, not carried a fourth week.
- **"Add GA4 via Rela's native GA-ID field"** — **CLOSED, not carried.** Plan-locked behind
  Plus/Pro (commit `2a1b0ad`), and the outcome it existed to achieve is already live:
  `G-95JF0FLSZH` confirmed loading via the Custom Script field again this run. Satisfied by
  workaround; revisit only if the owner upgrades the Rela plan. No week counter.
- **Rela support** (submitted via Rela chat 2026-09-10; chased 2026-09-11; still absent as of
  2026-09-16) — `twitter:card`, `og:url`, `og:locale`, H1 =
  "1550 Eastlake Ave E #503, Seattle, WA 98102" (currently "Apt 503, Seattle"), JSON-LD
  `numberOfBedrooms` (currently `numberOfRooms`), `amenityFeature`/`petsAllowed`/`containedInPlace`
  on the main node, `<img loading="lazy">`, `/sitemap.xml`=200, `robots.txt` without
  `Crawl-delay: 10` + with a `Sitemap:` line, `/llms.txt` populated.
- **/sitemap.xml** — once Rela ships it (200), submit under GSC → Sitemaps.
- **README channel name is stale** — `README.md` still says Slack `#real-estate-seo`; the confirmed
  channel is `#all-seo-eastlake` (`C0C0X36DRBQ`). Fix on the next README edit.
- **Redfin price discrepancy — owner can settle in 30 seconds.** A search-tool summary claimed the
  Redfin page for this address shows $698,000 against our $649,888. Redfin is bot-blocked so
  neither agent can verify it, and the tool's summaries have proven unreliable on this domain. Our
  own page is confirmed live at $649,888. If the owner wants certainty: open the Redfin page in a
  normal browser and look.

## Done 2026-09-16 (verified by Tier 1 this run)

- **No platform-side regression, third week running** — title, meta description, canonical, all
  og/twitter tags, both JSON-LD blocks, H1, image counts and both GA tags are byte-for-byte
  identical to 2026-09-14. Nothing Rela-side has reverted the owner's 2026-09-10 edits. A
  `last-modified` header bump with no field change was flagged and read as a platform cache touch.
- **Indexable confirmed YES** — HTTP 200, no `X-Robots-Tag` (checked on both the page and
  `/llms.txt` responses), no `<meta name="robots">`, self-referencing canonical in both the HTML tag
  and the HTTP `Link` header. Nothing on the page blocks Google.
- **"Baseline page speed" — CLOSED as unavailable by design.** Third consecutive 429 from the public
  PageSpeed quota, which was the pre-agreed trigger to stop asking. Removed from the queue; would
  need a real API key to revisit.
- **`gtag_token_occurrences` confirmed as noise** — measured 10 / 6 / 10 across three runs on an
  unchanged page. Retained as a diff aid only, never as a metric.

## Done 2026-09-14 (verified by Tier 1)

- **No platform-side regression, second week running** — all fields byte-for-byte identical to
  2026-09-11.
- **Both GA4 tags still live** — `G-1RVXDXERNN` (Rela's own) and `G-95JF0FLSZH` (owner's, via
  Custom Script), each confirmed loading via its own `googletagmanager.com/gtag/js?id=` script.
- **`indexed: no` retired as a recorded fact** — replaced with `inconclusive`. The `site:` and
  exact-phrase queries the old verdict rested on are now demonstrated not to work against this
  domain with the available search tooling. Only GSC can settle it (Do-now item 2).

## Done 2026-09-11 (verified by Tier 1)

- **GA4 tracking live on the page** — `G-95JF0FLSZH` confirmed present and loading. Delivered via
  the Custom Script field; see the plan-locked note above for why the native-field variant is closed.
- **`twitter:image:alt`** — confirmed present with descriptive text
  (`1550 Eastlake Ave E Apt 503, Seattle, WA | 2 Bed, 2 Bath`), off the Rela pending list.
- **All 2026-09-10 on-page edits confirmed still live and unreverted.**

## Done 2026-09-10 (via Chrome / Rela editor + GSC)

- SEO & Social: browser title, Google title+desc, Facebook OG, X/Twitter — all set with
  "Riva Condos"/"Riva Condominium" + "condo for sale" + MLS# 2556157. **LIVE.**
- Property Description: rewritten to name Riva Condominium / Riva Condos / Riva at Lake Union
  + South Lake Union. **LIVE.**
- Year Built: 2004 → 1997 (MLS# 2556157 confirmed) in the field + description. **LIVE.**
- Amenities: 7 → 12 (added Open Floor Plan, Oversized Windows, Private Balcony, Storage Unit,
  Lake Union Views; fixed trailing-period typo). **LIVE.**
- Custom Script (Advanced): injected a supplementary `ApartmentComplex` JSON-LD node for
  "Riva Condominium" (alternateName Riva Condos / Riva at Lake Union, yearBuilt 1997,
  numberOfFloors 5, address, geo, 4 amenityFeature). Valid, rendering. **LIVE** (2 JSON-LD
  blocks on page now).
- GSC: URL reported as indexed. "Request Indexing" clicked on the updated page.
- GA4: property created (Measurement ID G-95JF0FLSZH), added via Custom Script. **LIVE.**
