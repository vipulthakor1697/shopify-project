# Domayn Shopify Theme

A Shopify 2.0 theme recreating the [Domayn](https://vervhq.com/present-decks/domayn/) landing page — audio-visual neuromodulation, invite-only aesthetic.

## Project location

`/home/dd-03/Projects/domayn-theme`

## Quick start

1. Connect to your store:
   ```bash
   cd ~/Projects/domayn-theme
   shopify theme dev --store your-store.myshopify.com
   ```

2. Push to your store:
   ```bash
   shopify theme push --store your-store.myshopify.com
   ```

3. In **Shopify Admin → Online Store → Themes**, publish the Domayn theme.

## Theme structure

| Section | Purpose |
|---------|---------|
| `header` | Fixed nav with logo, menu, invite link |
| `hero` | Full-viewport hero with overlay copy |
| `data-row` | Statistics strip |
| `manifesto` | “Interior. Under control.” |
| `product-object` | Product flat-lay image |
| `protocols` | Wake / Focus / Relax / Sleep accordion |
| `session-feel` | Session imagery |
| `brain-rhythm` | Science + 3-step explainer |
| `testimonials` | Voice quotes |
| `campaign` | Campaign imagery |
| `origins` | Five-chapter tabbed story |
| `faq` | Essentials accordion |
| `cta-waitlist` | Final CTA + email capture |
| `footer` | Links + disclaimers |

## Setup checklist

1. **Navigation** — Create menus in Admin → Content → Menus:
   - Main menu: The Mask, The Science, The Lab
   - Footer menus: Pages + Legal links

2. **Images** — Upload via the theme editor (recommended from the reference deck):
   - Hero: person on stone slab in dark hall
   - Product object: blue flat-lay of the Mask
   - Session feel: macro of mask knit texture
   - Campaign: monolith chamber portrait
   - Origins tabs: five pencil sketch images

3. **Fonts** — Theme Settings → Typography:
   - Heading: Fraunces (or similar serif)
   - Body: Assistant / Hanken Grotesk (sans-serif)

4. **Colors** — Defaults match the reference (ink `#0E1230`, paper `#F7F8FA`, accent `#1B2DFF`).

5. **Waitlist** — The CTA form uses Shopify’s customer form with a `waitlist` tag. Subscribers appear in **Customers**.

## Code rules (followed)

- Every section has a `{% schema %}` block
- CSS scoped with `#shopify-section-{{ section.id }}`
- Images use `image_url` + lazy loading
- No inline styles, hardcoded colors, or hardcoded copy in Liquid
- Accessible buttons (`aria-label`) and image `alt` text
- Mobile-first CSS

## CSS variables

Defined in `layout/theme.liquid` and used across sections:

- `--color-base-text`
- `--color-base-background-1`
- `--color-base-accent-1`
- `--font-body-family`
- `--font-heading-family`
