# ACTION QUEUE — eastlakeview503.relahq.com

Executable to-do for a browser session (Claude in Chrome, logged into Rela + Google).
Tier 2 rewrites this file each week. Top section = do now.

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
- GSC: URL is indexed (confirmed). "Request Indexing" clicked on the updated page.

## Do now

_(next browser session)_

1. **Add GA4 to Rela** — Rela → Advanced → "Google Analytics or Google Tag Manager ID":
   paste the user's `G-XXXXXXX` Measurement ID. (Blocked: need the ID from the user.)
2. **Extend the Custom-Script JSON-LD with a full `RealEstateAgent` node** once the user
   supplies agent phone + brokerage name + headshot URL. Append to the existing
   `<script type="application/ld+json">` block in Rela → Advanced (make it an `@graph` with
   both the ApartmentComplex and the RealEstateAgent). (Blocked: need agent details.)

## Backlog / blocked

- **Inbound links** (owner) — place links to `https://eastlakeview503.relahq.com/` from:
  brokerage agent-profile page, personal agent bio, email signature, LinkedIn (Featured +
  a "just listed" post), Instagram bio, a Seattle/Eastlake real-estate Facebook group.
  Anchor text: "1550 Eastlake Ave E #503 — Riva Condominium" or "Riva Condos #503, Eastlake".
  THIS IS THE #1 RANKING LEVER — the page is indexed but has zero inbound links.
- **Rela support** (submitted via Rela chat 2026-09-10, "team back in 1 hour") — chase if the
  pending template items haven't landed after 2 weeks: `twitter:card`, `og:url`, `og:locale`,
  `twitter:image:alt` fix, H1 = "1550 Eastlake Ave E #503, Seattle, WA 98102", JSON-LD
  `numberOfBedrooms` (currently `numberOfRooms`), `<img loading="lazy">`, `/sitemap.xml`=200,
  `robots.txt` without `Crawl-delay: 10` + with `Sitemap:` line, `/llms.txt` populated.
- **/sitemap.xml** — once Rela ships it (200), submit under GSC → Sitemaps.
