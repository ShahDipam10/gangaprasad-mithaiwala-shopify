# Gangaprasad Mithaiwala — Master Shopify Store Prompt

This is the complete specification for the project — everything decided so
far, plus everything a typical modern, production-grade Shopify store needs
that hasn't been explicitly covered yet. Treat this as the single source of
truth: if you're regenerating the design, use this in full. If you're
briefing a developer, this is the spec they build against.

**Purpose**: this is a portfolio piece for a two-person Shopify agency. It
needs to look and function like a real, live client store — something you'd
put in front of a prospective client to prove the agency can build a
complete, professional Shopify site, not a partial demo.

---

## 1. Brand

**Gangaprasad Mithaiwala** — a Gujarati mithai (sweets) and namkeen (savory
snacks) shop, founded 1919 in Anand, Gujarat (India's dairy capital), run by
the same family for three (going on four) generations. Fresh cow's milk
sourced daily from local dairy cooperatives, no preservatives, small daily
batches. Positioning: "if Haldiram launched an Apple-designed premium
Shopify store" — heritage, warmth, and craft, not a generic bakery template.

- **Tagline**: "A sweet relation, since 1919."
- **Logo**: circular seal mark — double gold ring, italic serif "GM"
  monogram, "Est. 1919" — used in header, footer, and mobile nav.
- **Palette**: maroon `#6B1229` (primary), deep maroon `#4A0C1C` (footer/
  dark sections), saffron `#E8912F` (accent/CTAs), gold `#B8860B` /
  `#C9971F` (dividers, small ornament — used sparingly), cream `#FBF4E8`
  (page background), warm neutral `#F3E7D2` (card/section tint), jade
  `#1F6F5C` (trust accent).
- **Type**: Fraunces (serif, headings/logo) + Poppins (sans, body/UI).
- **Photography**: real photography throughout — no illustrated/AI-looking
  placeholders. Real CC-licensed photos (e.g. Wikimedia Commons) are an
  acceptable stand-in for products not yet professionally shot, but must be
  flagged as a stand-in (a small "stand-in photo" badge) rather than
  presented as final.
- **Currency**: Indian Rupees (₹) throughout — this is an India-market
  store. COD and UPI/Razorpay/Cashfree-style payment expectations, not
  Shopify Payments (unavailable in India).

## 2. Full site architecture

Every one of these needs to exist and be reachable — not just the "hero"
pages.

**Primary pages**
- Home
- Collections: Sweets, Namkeen, Festival Specials (one template, three
  collections)
- Product detail (one template, all products)
- About (heritage story + timeline)
- Contact (form + store info + map)
- FAQ (accordion)
- Policy pages: Privacy, Terms of Service, Refund, Shipping (native Shopify
  legal pages, not a custom single tabbed page)
- Cart (drawer, not just a separate page)
- Search results page

**States that a "typical Shopify store" also needs** (easy to forget, easy
to spot as missing in a portfolio review):
- Empty cart state
- Empty search results state
- 404 page
- Out-of-stock product state
- Order confirmation expectations (native Shopify checkout — note where
  custom messaging like "COD available" should appear pre-checkout, since
  checkout itself isn't deeply customizable without Shopify Plus)

**Customer account pages** (Shopify's native account system): login/
register, order history, addresses. Doesn't need custom design work beyond
matching the brand's color scheme/typography — but shouldn't be left at
Shopify's raw default styling.

## 3. Global components

- **Header**: centered logo, inline nav (Home / Sweets / Namkeen / Festival
  Specials / About / Contact), **mega menu on hover** for the three
  collection items — shows the collection's photo plus its top 3 products
  with price. Search icon opening a **predictive search** (live results
  with product thumbnails as you type, not just a plain search box). Cart
  icon with live item count, opening a **cart drawer** (not a full page
  redirect) showing line items, quantity controls, subtotal, and a
  checkout button. Mobile: full-screen nav drawer.
- **Footer**: logo + tagline, address/phone/hours, "Trusted Since 1919"
  certification list (FSSAI certified, 3rd-generation family run, no
  preservatives, fresh daily, pan-India shipping/COD), a static
  illustrative map (no API key needed), policy links, social links,
  payment method icons.
- **Trust signals**, used consistently across product cards and the product
  page: star rating + review count, "No preservatives," "Fresh daily
  batch," "COD available."

## 4. Page-by-page requirements

**Home**: photo hero (real photography, not illustration) with heading/
subheading/CTA, Shop by Category (3 real collection cards), Bestsellers
(real product grid with ratings + bestseller badges), Shop by Occasion
(Wedding/Corporate/Festival/Everyday gifting), Our Story heritage section.

**Collection**: breadcrumb, collection title + intro copy, product count,
**filters** (by weight, by price range) and **sort** (Featured / Price low-
high / Price high-low), responsive product grid, pagination, an empty
state if a filter combination returns nothing.

**Product detail**: image gallery with thumbnails, star rating + review
count, price, weight/size variant selector, quantity, Add to Cart (sticky
on mobile once you scroll past the gallery), trust badges row, Ingredients
and Shelf Life (from real product data, not buried in a generic
description), Customer Reviews section, Related Products, "Frequently
bought together"-style cross-sell if time allows.

**Cart drawer**: line items with thumbnail/name/variant/price/quantity
controls, subtotal, a note about COD/shipping estimate, checkout button.

**Search**: predictive/live results as you type; a full results page for
submitted searches, with the same filter/sort pattern as collections; a
clear empty state ("No results for '...' — try Sweets or Namkeen") rather
than a blank page.

**About**: hero image with overlay heading, founding story (1919, Anand,
dairy cooperatives), founder/family photo (flagged stand-in if not real),
a 4-chapter timeline (1919 → 1958 → 1994 → Today).

**Contact**: form (name/email/message), address/phone/hours, static
illustrative map.

**FAQ**: accordion — shelf life, shipping/COD, returns on perishables, bulk
orders, allergens.

**Policy pages**: native Shopify Privacy/Terms/Refund/Shipping pages with
real, specific copy (not generic legal boilerplate) — e.g. the refund
policy should explicitly address perishable goods.

## 5. Content rules

- No lorem ipsum, anywhere.
- Real product data: name, price (₹), weight variants, ingredients, shelf
  life, a short and long description — for every product, not just the
  bestsellers.
- Every image needs real alt text.
- SEO: meta title + description per page, clean URLs (Shopify defaults are
  fine), product structured data (Shopify handles this natively via theme
  best practices — don't strip it out).

## 6. Technical/quality bar

- **Mobile-first**: designed and built mobile-first, desktop is the
  enhancement, not the other way around.
- **Performance**: optimized images, lazy loading below the fold, minimal
  unnecessary JS.
- **Accessibility**: real alt text, sufficient color contrast, keyboard-
  navigable menus and forms, visible focus states.
- **No AI-generated-design tells**: no generic centered-hero-with-gradient
  look, no cookie-cutter icon rows, no placeholder photography presented as
  final.

## 7. What "done" looks like

Someone unfamiliar with the project should be able to land on the home
page, browse a collection, open a product, understand shipping/COD/
freshness expectations, add to cart, and find the FAQ/policies/contact
info — all without hitting a dead end, a stub page, or an obviously-fake
placeholder. It should read as a real, live, professionally built Shopify
store for an Indian sweets brand, not a partial demo.
