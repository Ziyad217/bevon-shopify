# bevon — Premium Football Streetwear

Custom Shopify theme for **bevon** — German football streetwear brand for the FIFA World Cup 2026.

Built on the [Shopify Dawn](https://github.com/Shopify/dawn) theme baseline, customized with a light/clean/sporty design direction (white + sporty blue `#0066CC`).

---

## Brand identity

- **Tagline:** Premium Football Streetwear — Designed in Deutschland
- **Audience:** German football fans, 16–30, streetwear-affine
- **Default language:** German (`de`)
- **Currency:** EUR

## Design tokens

| Token | Value |
|-------|-------|
| Background | `#FFFFFF` |
| Surface | `#F5F5F5` |
| Foreground | `#1A1A1A` |
| Accent (primary) | `#0066CC` |
| Accent hover | `#0052A3` |
| Border | `#E5E5E5` |
| Heading font | Inter / Montserrat (uppercase, bold) |
| Body font | Inter |
| Border radius | 8px (md) |

All tokens live in [`assets/bevon-custom.css`](assets/bevon-custom.css) under `:root`.

## Custom homepage sections

The homepage (`templates/index.json`) is built from these custom bevon sections:

| Order | Section | File |
|---|---|---|
| 1 | Hero with CTA + urgency | [`sections/bevon-hero.liquid`](sections/bevon-hero.liquid) |
| 2 | Featured bestseller spotlight | [`sections/bevon-featured-product.liquid`](sections/bevon-featured-product.liquid) |
| 3 | "Meistgefragte Designs" 3-col grid | [`sections/bevon-product-grid.liquid`](sections/bevon-product-grid.liquid) |
| 4 | Trust-Bar (4 icons) | [`sections/bevon-trust-bar.liquid`](sections/bevon-trust-bar.liquid) |
| 5 | Horizontal product carousel | [`sections/bevon-product-carousel.liquid`](sections/bevon-product-carousel.liquid) |
| 6 | "Premium Kollektionen" numbered grid | [`sections/bevon-collection-grid.liquid`](sections/bevon-collection-grid.liquid) |
| 7 | "The New Season" auto-scroll marquee | [`sections/bevon-image-marquee.liquid`](sections/bevon-image-marquee.liquid) |
| 8 | Countdown / urgency block | [`sections/bevon-countdown.liquid`](sections/bevon-countdown.liquid) |
| 9 | Marquee text ticker | [`sections/bevon-text-ticker.liquid`](sections/bevon-text-ticker.liquid) |
| 10 | Newsletter (Dawn extended) | `sections/newsletter.liquid` |

Header, announcement bar, and footer are managed via Dawn's `header-group.json` and `footer-group.json`.

## Page templates

Custom German page templates:

- `templates/page.about.json` — Unsere Story
- `templates/page.faq.json`
- `templates/page.impressum.json`
- `templates/page.datenschutz.json`
- `templates/page.agb.json`
- `templates/page.versand.json`
- `templates/page.contact.json` *(Dawn default, kept)*

After installing the theme, create matching Pages in Shopify Admin → *Online Store → Pages → Add Page*. Set the Theme template dropdown to the matching custom template.

---

## Connect this repo to Shopify

This repo is designed to be installed into Shopify via GitHub integration. Once connected, every push to `main` auto-syncs to the live theme.

### One-time setup

1. Open your Shopify Admin → **Online Store → Themes**.
2. Click **Add theme → Connect from GitHub**.
3. Authorize the Shopify app on GitHub if prompted.
4. Select repository **`Ziyad217/bevon-shopify`**.
5. Select branch **`main`**.
6. Click **Connect**.

The theme will appear in your theme library as "bevon-shopify". To go live, click **Actions → Publish**.

### Working locally

```bash
# Clone
git clone https://github.com/Ziyad217/bevon-shopify.git
cd bevon-shopify

# Live preview against your dev store
shopify theme dev --store <your-store>.myshopify.com

# Validate before pushing
shopify theme check
```

### Sync flow

```
local edit → git push origin main → Shopify auto-pulls within ~1 min
```

If a push doesn't sync, check the connection in Shopify Admin → **Online Store → Themes → bevon-shopify → Edit code** (the "GitHub-managed" badge should be visible).

---

## Assets to add

The theme ships with placeholders for these assets — replace via Shopify Admin → *Online Store → Themes → Customize*:

- **Logo:** Header logo (recommended ~360×80px PNG with transparent bg)
- **Hero image:** Section "bevon Hero" (recommended 2400×1200px)
- **Featured bestseller image:** Auto-pulls from selected product
- **Collection images:** Auto-pulls from each Collection's image (set via *Products → Collections → [collection]*)
- **Lifestyle marquee images:** Section "bevon Lifestyle-Marquee" (recommended 800×1000px each)

---

## Credits

Built on [Shopify Dawn](https://github.com/Shopify/dawn) (MIT). Original Dawn license preserved in `LICENSE.md`.
