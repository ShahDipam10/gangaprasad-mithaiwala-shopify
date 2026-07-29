# Gangaprasad Mithaiwala — Shopify Store

Shopify storefront for **Gangaprasad Mithaiwala**, a century-old Gujarati
mithai (sweet) and namkeen manufacturer based in Anand, Gujarat. Built on
Shopify's free **Dawn** theme, customized for a festive, heritage-driven
brand identity.

Full requirements: [docs/Project-Brief.md](docs/Project-Brief.md).
Dawn's original theme docs (architecture, dev commands): [docs/DAWN_THEME.md](docs/DAWN_THEME.md).

## Store

- Dev store: `gangaprasad-mithaiwala.myshopify.com`
- Shopify Partners org: DivineDevelopers (org id `228741837`)

## Stack

- Shopify Dawn theme (Liquid, sections/blocks, vanilla JS/CSS)
- Shopify CLI for local theme dev / preview / deploy

## Getting started

```bash
npm install -g @shopify/cli @shopify/theme
shopify theme dev --store gangaprasad-mithaiwala.myshopify.com
```

This opens a local preview that hot-reloads as you edit theme files, backed
by the real dev store's data (no changes go live on a real storefront —
it's a sandboxed dev store).

## Status

Early scaffold — see open tasks / commits for current progress.
