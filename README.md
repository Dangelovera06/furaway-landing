# Furaway — Shopify theme

Converted from the static Furaway site. Drop this folder into Shopify as a theme.

## Install

1. Zip the **contents** of this `shopify-theme` folder (so `layout/`, `templates/`, `assets/`, etc. are at the root of the zip — not nested inside a `shopify-theme/` folder).
2. Shopify Admin → **Online Store → Themes → Add theme → Upload zip file**.
3. After it uploads, click **Customize** to set the featured product.

## One-time setup in Shopify

1. **Create the product** (Products → Add product). Suggested:
   - Title: `The Pet Hair Remover` (or `FA-01 Pet Hair Remover`)
   - Price: `$29` (set compare-at to `$39` if you want the "Save 25%" pill)
   - Upload product images (hero, colors, bed, product, studio)
   - Add a **Color** option with values `Sage`, `Blush`, `Sky`, `Cloud`
   - Optionally add a **Bundle** option with values `Single`, `Duo`, `Family`
   - One variant per combination; set prices per bundle
2. **Set featured product** — Online Store → Themes → Customize → Theme settings → General → Featured product.
3. **Menu** — Online Store → Navigation → `main-menu` should have: How it works (`/#how`), Colors (`/#colors`), Shop (`/collections/all` or product url), FAQ (`/#faq`).
4. **Set homepage** — Online Store → Preferences → set the homepage to use the default template (which is `templates/index.liquid` from this theme).

## What's wired up

- **Homepage** (`templates/index.liquid`): static marketing content, CTA links to the featured product.
- **Product page** (`templates/product.liquid`): real Shopify product/variant picker, real Add to Cart form, dynamic price.
- **Cart, Collection, 404, Search, Page** templates included.
- **Header / Footer** are sections with editable settings.

## What's intentionally minimal

- No cart drawer / AJAX cart — the form posts to `/cart/add` and uses the standard `/cart` page.
- Reviews are hardcoded copy (the original site's design). Hook up a reviews app (Judge.me, Yotpo, Shopify Product Reviews) and replace the rating block when ready.
- The "bundle" UI on the original mock is now driven by product variants. Add a `Bundle` option in the product to bring it back.

## Local files preserved

The static site is still at `furaway/index.html` and `furaway/product.html` — this theme lives alongside it in `furaway/shopify-theme/`.
