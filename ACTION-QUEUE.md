# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do for a browser session (Claude in Chrome, logged into Rela + Google).
Tier 2 rewrites this file each week. Top section = do now.

## Do now

_(week of 2026-09-14 — full copy/paste text in `reports/STRATEGY-2026-09-14.md` §2)_

1. **Place the first inbound links** (60–90 min) *(carried 1 week)*. The page still has **zero**
   external links pointing to it — the single biggest lever available. Email signature, LinkedIn
   (Featured + one post), Instagram bio, brokerage agent-profile page, personal bio page, one
   Seattle/Eastlake real-estate Facebook group. Link text every time:
   `1550 Eastlake Ave E #503 — Riva Condominium`. Post copy is in the strategy memo §2.1.
   Report roughly which placements landed in Slack so this item can close.
2. **Settle the Search Console question, once** (10 min) *(carried 1 week)*. GSC → pick the
   `eastlakeview503.relahq.com` property → paste `https://eastlakeview503.relahq.com/` into the top
   search bar → Enter. Write down the exact headline ("URL is on Google" / "URL is not on Google" /
   "URL is available to Google"), click **Request Indexing** if it is not indexed, then open
   **Indexing → Pages** and note the "Not indexed" count and top reason. Report both in Slack.
   **This is verification, not an alarm** — nothing on the page blocks indexing, and GSC itself said
   indexed on 2026-09-10. This item closes after this week either way.
3. **Put descriptions on the 19 listing photos** (20–30 min). 0 of 19 property photos have alt
   text; the only 3 alt attributes on the page are on logos. Rela → listing → **Photos** → check
   each photo for an **Alt text / Description / Caption** field and fill it in describing what is
   actually visible (12 ready-to-adapt lines in the memo §2.3 — vary them, do not paste one line 19
   times). **If no such field exists**, it is platform-side: paste the Rela support message in the
   memo §2.3, which also chases the sitemap/robots items below.

## Next up (not this week)

- **Chase Rela on the sitemap + robots.txt** *(carried 1 week)*. `/sitemap.xml` still 404,
  `robots.txt` still `Crawl-delay: 10` with no `Sitemap:` line — Tier 1 confirms **NOT DONE**.
  Deliberately not its own Do-now slot: for a one-page site a sitemap is close to cosmetic and
  Google ignores `Crawl-delay`. Folded into the Rela support message in Do-now item 3.
- **Link the two JSON-LD nodes.** The unit (`Apartment`) and building (`ApartmentComplex`) nodes
  both exist but are not connected, so Google is not told that unit #503 is inside Riva
  Condominium. Fix means adding `containedInPlace` in Rela → Advanced → Custom Script. Do it in the
  same editing pass as the `RealEstateAgent` node below, not on its own.
- **Baseline page speed.** Two runs, two 429s from the public PageSpeed quota — no Core Web Vitals
  number has ever been captured. If it 429s a third time next week, treat as unavailable by design
  and stop asking.

## Backlog / blocked

- **Inbound links** (owner) — promoted to "Do now" item 1. Still the **#1 ranking lever**: the page
  has zero external links pointing to it.
- **Extend the Custom-Script JSON-LD with a full `RealEstateAgent` node** — Tier 1 confirms **NOT
  DONE** again on 2026-09-14 *(carried 2 weeks)*. ⚠️ **Crosses the 3-week threshold next Monday.**
  Blocked, not hard: needs **agent phone + brokerage name + headshot URL** from the owner. The only
  agent data on the page is still `name` + `email` (`Omar Senghor`, `change-re@outlook.com`) on the
  `Apartment` node's `provider`. **Owner: send those three details and this becomes a 10-minute
  job.** If they are not supplied by 2026-09-21, this gets cut or rewritten as a smaller
  "add the phone number only" step.
- **"Add GA4 via Rela's native GA-ID field"** — **CLOSED, not carried.** Plan-locked behind
  Plus/Pro (commit `2a1b0ad`), and the outcome it existed to achieve is already live:
  `G-95JF0FLSZH` confirmed loading via the Custom Script field again this run. Satisfied by
  workaround; revisit only if the owner upgrades the Rela plan. No week counter.
- **Rela support** (submitted via Rela chat 2026-09-10; chased 2026-09-11; still absent as of
  2026-09-14) — `twitter:card`, `og:url`, `og:locale`, H1 =
  "1550 Eastlake Ave E #503, Seattle, WA 98102" (currently "Apt 503, Seattle"), JSON-LD
  `numberOfBedrooms` (currently `numberOfRooms`), `amenityFeature`/`petsAllowed`/`containedInPlace`
  on the main node, `<img loading="lazy">`, `/sitemap.xml`=200, `robots.txt` without
  `Crawl-delay: 10` + with a `Sitemap:` line, `/llms.txt` populated.
- **/sitemap.xml** — once Rela ships it (200), submit under GSC → Sitemaps.
- **README channel name is stale** — `README.md` still says Slack `#real-estate-seo`; the confirmed
  channel is `#all-seo-eastlake` (`C0C0X36DRBQ`). Fix on the next README edit.

## Done 2026-09-14 (verified by Tier 1 this run)

- **No platform-side regression, second week running** — title, meta description, canonical,
  all og/twitter tags, both JSON-LD blocks, H1, image counts and both GA tags are byte-for-byte
  identical to 2026-09-11. Nothing Rela-side has reverted the owner's 2026-09-10 edits.
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
