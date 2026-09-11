# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do for a browser session (Claude in Chrome, logged into Rela + Google).
Tier 2 rewrites this file each week. Top section = do now.

## Do now

_(week of 2026-09-11 — full copy/paste text in `reports/STRATEGY-2026-09-11.md` §2)_

1. **Check in Google Search Console whether the page is actually indexed** (10 min).
   GSC → pick the `eastlakeview503.relahq.com` property → paste
   `https://eastlakeview503.relahq.com/` into the top search bar → Enter. Note the exact headline
   ("URL is on Google" / "URL is not on Google" / "available to Google"), click **Request Indexing**
   if it is not indexed, then open **Indexing → Pages** and note the "Not indexed" count and top
   reason. Report both back in Slack. **Nothing else matters until this is known** — the page
   appeared in zero of 5 tracked queries and returned zero results for `site:` this week.
2. **Place the first inbound links** (60–90 min). Email signature, LinkedIn (Featured + one post),
   Instagram bio, brokerage agent-profile page, personal bio page, one Seattle/Eastlake real-estate
   Facebook group. Link text every time:
   `1550 Eastlake Ave E #503 — Riva Condominium`. Post copy is in the strategy memo.
3. **Chase Rela on the sitemap + robots.txt** (5 min). Rela support chat; exact message in the
   strategy memo §2.3. `/sitemap.xml` is 404 and `robots.txt` has `Crawl-delay: 10` with no
   `Sitemap:` line — the sitemap is the part that genuinely matters.

## Next up (not this week)

- **Alt text on the 19 property photos.** 0 of 19 currently have any; the only 3 alt attributes on
  the page are on logos. In Rela → Photos, check whether each photo has a caption/description/alt
  field. If it does, fill it in describing what is actually visible, e.g.
  `Lake Union and Seattle skyline view from the private balcony of 1550 Eastlake Ave E #503`.
  If there is no such field, add it to the Rela support list instead — it is then platform-side.
- **Link the two JSON-LD nodes.** The unit (`Apartment`) and the building (`ApartmentComplex`) nodes
  both exist but are not connected, so Google is not told that unit #503 is inside Riva Condominium.
  Fixing this means adding `containedInPlace` in the Rela → Advanced → Custom Script block. Do it in
  the same editing pass as the `RealEstateAgent` node below, not on its own.

## Backlog / blocked

- **Inbound links** (owner) — promoted to "Do now" item 2 this week. Still the **#1 ranking lever**:
  the page has zero external links pointing to it.
- **Extend the Custom-Script JSON-LD with a full `RealEstateAgent` node** — Tier 1 confirmed
  **NOT DONE** on 2026-09-11 *(carried 1 week)*. Blocked: needs agent phone + brokerage name +
  headshot URL from the owner. The only agent data on the page is still `name` + `email`
  (`Omar Senghor`, `change-re@outlook.com`) on the `Apartment` node's `provider`. **Owner: send
  those three details and this becomes a 10-minute job.**
- **"Add GA4 via Rela's native GA-ID field"** — *(carried 1 week)*, and moved here from "Do now"
  because it is **plan-locked, not pending**: Rela's Google Analytics ID field requires Plus/Pro
  (commit `2a1b0ad`). The outcome it existed to achieve is already live — `G-95JF0FLSZH` was
  confirmed loading on the page this run via the Custom Script field. Tier 1 records this as
  "CANNOT VERIFY FROM PAGE" because native-field and Custom-Script injection emit identical markup,
  so it cannot be closed by observation. Treat it as satisfied-by-workaround; revisit only if the
  owner upgrades the Rela plan. Not worth carrying as an open task.
- **Rela support** (submitted via Rela chat 2026-09-10; chased 2026-09-11 as "Do now" item 3) —
  still absent as of 2026-09-11: `twitter:card`, `og:url`, `og:locale`, H1 =
  "1550 Eastlake Ave E #503, Seattle, WA 98102" (currently "Apt 503, Seattle"), JSON-LD
  `numberOfBedrooms` (currently `numberOfRooms`), `amenityFeature`/`petsAllowed`/`containedInPlace`
  on the main node, `<img loading="lazy">`, `/sitemap.xml`=200, `robots.txt` without
  `Crawl-delay: 10` + with a `Sitemap:` line, `/llms.txt` populated. `twitter:image:alt` is now
  present and descriptive — that one landed.
- **/sitemap.xml** — once Rela ships it (200), submit under GSC → Sitemaps.

## Done 2026-09-11 (verified by Tier 1 this run)

- **GA4 tracking live on the page** — `G-95JF0FLSZH` confirmed present and loading (alongside
  Rela's own `G-1RVXDXERNN`). Delivered via the Custom Script field; see the plan-locked note above
  for why the native-field variant stays in the backlog.
- **`twitter:image:alt`** — confirmed present with descriptive text
  (`1550 Eastlake Ave E Apt 503, Seattle, WA | 2 Bed, 2 Bath`), off the Rela pending list.
- **All 2026-09-10 on-page edits confirmed still live and unreverted** — title, meta description,
  og/twitter tags, `yearBuilt` 1997, `offers.price` 649888, the injected `ApartmentComplex` JSON-LD
  block. No platform-side regression.

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
- GSC: URL reported as indexed. "Request Indexing" clicked on the updated page. **Note: contradicted
  by the 2026-09-11 `site:` check, which returned zero pages — re-verify (Do now item 1).**
- GA4: property created (Measurement ID G-95JF0FLSZH), added via Custom Script. **LIVE.**
