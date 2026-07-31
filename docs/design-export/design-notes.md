# Gangaprasad Mithaiwala — Shopify Storefront Mockup

Mobile-first Shopify-style storefront mockup for a fictional heritage mithai (Indian sweets) & namkeen shop, est. 1919, Anand, Gujarat.

**File:** `Gangaprasad Mithaiwala.dc.html`

## Brand
- Palette: maroon `#6B1229` / deep maroon `#4A0C1C`, saffron/gold accent `#E8912F`, antique gold `#B8860B`/`#C9971F`, cream background `#FBF4E8`, warm neutral `#F3E7D2`, jade green `#1F6F5C` for trust accents.
- Type: Fraunces (serif, headings/logo) + Poppins (sans, body/UI).
- Logo: custom circular seal — double gold ring on maroon (or cream, inverted for dark backgrounds) with an italic "GM" monogram and a thin rule beneath. Used in header, mobile menu, and footer.
- Tagline: "A sweet relation, since 1919."

## Pages (all in one Design Component, client-side routed)
1. **Home** — hero image slider (4 crossfading photos with custom arrow buttons + dot indicators), horizontal-scroll "Shop by Category" carousel, Bestsellers grid (pedestal-style circular product shots), "Our Story" heritage strip, footer.
2. **Collection** (Sweets / Namkeen / Festival Specials) — breadcrumb, sort controls (Featured / Price), responsive product grid.
3. **Product detail** — image gallery with thumbnails, weight-variant selector, add-to-cart, ingredients/shelf-life accordlocal sections, related products.
4. **About** — heritage story, founder/family photo placeholder (flagged stand-in), 4-chapter timeline (1919 → today).
5. **Contact** — form + address/phone.
6. **FAQ** — accordion (shipping, COD, returns policy on perishables, bulk orders, allergens).
7. **Policies** — tabbed Privacy / Terms / Refund / Shipping copy.

## Header & Navigation
- 3-zone header: nav (desktop) / hamburger (mobile) on the left, centered logo, search bar (with rotating placeholder copy: "Find your sweet today...", "Craving something sweet?", etc.) + cart icon on the right.
- Mobile menu: full-screen maroon panel with logo, nav list, "Shop Bestsellers" CTA, and a contact line. No FAQ/Policies clutter.

## Footer
- Left: logo + tagline + shop address + phone/hours.
- Middle: "Trusted Since 1919" certification list (FSSAI, 3rd-gen family run, no preservatives, pan-India shipping/COD).
- Right (bottom on mobile): static, no-API illustrative map graphic with a pin marking the Anand, Gujarat location.

## Imagery
- All real photography (no hand-drawn SVG scenes), sourced from Wikimedia Commons (CC-licensed) — kaju katli, doodh peda, motichoor laddu, jalebi, Gujarati farsan, khakhra, festive mithai platters, and a mithai shop storefront.
- Items without a strong matching real photo are explicitly flagged "Stand-in photo" / "Photo pending" in the UI — a real product shoot is recommended before launch (mohanthal, doodh barfi, some namkeen/festival SKUs).
- Background-image (not `<img src>`) is used for all data-driven product/category photos — the DC template engine resolves remote URLs correctly this way for dynamic values.

## Content system
- 11 SKUs across Sweets / Namkeen / Festival Specials, each with description, ingredients, shelf life, and weight-based pricing (₹).
- Trust badges: No preservatives, Fresh daily batches, 3rd-generation family run, FSSAI certified, COD available, Pan-India shipping.

## Known follow-ups / open items
- Several product and lifestyle photos are still stand-ins pending a real shoot (see "Stand-in photo" tags in the Collection/Product pages).
- Map is a static illustrative graphic, not a live/interactive map (per requirement: no API key).
- Cart and search are visual/UI only — no real commerce logic wired up (this is a design mockup, not a live Shopify build).
