# Gangaprasad Mithaiwala — Shopify Store

A Shopify theme project for Gangaprasad Mithaiwala, a century-old Gujarati
mithai/namkeen manufacturer. Full brief: [docs/Project-Brief.md](docs/Project-Brief.md).
Agency context (who's building this and how they like to work): [docs/Agency-Onboarding.md](docs/Agency-Onboarding.md).

## Hard rules

1. **Never commit secrets.** No Shopify Admin API tokens, Razorpay/Cashfree
   keys, or any password/credential goes into git, ever — not even in
   comments or example configs. Use a local `.env` (gitignored) for
   anything sensitive, or better, Shopify CLI's browser-based OAuth login
   (`shopify auth login` / `shopify theme dev`) which needs no password.
2. **This is a two-person learning agency project** (see
   docs/Agency-Onboarding.md) — explain *why*, not just *what*, when making
   non-obvious theme/architecture decisions. They're beginners at Shopify
   dev specifically, but experienced with Git/GitHub/Playwright/QA — lean
   on that existing knowledge rather than over-explaining basics they
   already know from other stacks.
3. **Built on Dawn**, Shopify's free reference theme (Liquid + sections/
   blocks architecture). Customize via new sections/blocks/snippets rather
   than forking core Dawn logic where avoidable, so theme updates stay
   mergeable.
4. **No real payment/shipping credentials get wired up without an explicit
   go-ahead** — Razorpay/Cashfree/Shiprocket integrations should be scaffolded
   against docs/sandbox modes first; ask before pointing anything at a real
   merchant account.

## Store info

- Dev store: `gangaprasad-mithaiwala.myshopify.com`
- Shopify Partners org: DivineDevelopers (org id `228741837`)
- Theme base: Dawn (cloned from github.com/Shopify/dawn)

## Brand & design direction (from the brief)

- **Palette**: saffron orange, maroon/red, gold accents, jade green —
  festive Indian aesthetic, not a generic pastel bakery look.
- **Voice**: heritage/authenticity forward ("100+ years of tradition",
  Anand, Gujarat roots) — see docs/Project-Brief.md for full copy guidance.
- **Pages required**: Home, About, Collections (Sweets/Namkeen/Festival
  Specials), Product pages, Contact, FAQ, Policies, optional Blog.
- **India-specific commerce**: COD is expected by most customers, UPI/
  Razorpay/Cashfree for online payment, Shiprocket-style shipping app for
  courier rates — Shopify Payments itself isn't available in India.

## Working style

- Short, direct answers; explain reasoning for non-obvious calls per rule 2.
- Verify theme changes in the local `shopify theme dev` preview before
  calling something done — no automated test suite for theme code.
- Compile-check Liquid changes by loading the page in preview; watch the
  terminal for Liquid syntax errors on save.
