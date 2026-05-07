# Fortezza Coffee — Demo Website

Demo website for **Fortezza Coffee · Ke-Ki On-Ga** (Marco &amp; Sofia Castelli) — a heraldic Italian café at 215 E Berry St, downtown Fort Wayne, IN. The first café in Indiana to pour Caffè Vergnano espresso from Turin (1882), with house-made gelato, panini pressed under cast iron, and dolci from a Naples-trained baker.

This is a static, dependency-free site built by [Sweet Dreams Studios](https://sweetdreamsmusic.com) as a styling proposal.

## Brand notes

- **Name:** Fortezza Coffee — *fortezza* is Italian for *fortress*. The name honors both the Castelli family heritage in Northern Italy and the historic indigenous name for Fort Wayne, **Ke-Ki On-Ga** ("the village at the meeting of three rivers"), used by the Miami people who lived here before the Old Fort was built.
- **Mark:** A circular badge with a red cavaliere (cavalry rider) on horseback at the center, wrapped in a royal-blue arc that reads FORTEZZA above and KE-KI ON-GA below. See `assets/logo.svg`.
- **Voice:** Warm, Italian-American, neighborhood, lightly heraldic. Not stiff or formal.

## Pages

- `index.html` — hero, philosophy, three pillars (caffè / dolci / welcome), Vergnano feature, inside-the-fortress grid, stats, testimonials, location tease, final CTA
- `menu.html` — full menu: espresso, brew &amp; tea, gelato artigianale, panini, dolci, Vergnano beans-to-go
- `story.html` — Marco &amp; Sofia, Ke-Ki On-Ga explainer, four-chapter timeline, six values
- `visit.html` — address, hours, contact, Google Map embed, contact form, catering
- `order.html` — demo checkout flow with cart drawer + customizer sheet
- `404.html` — friendly fallback

## Stack

- Pure HTML / CSS / JS — no build step, no framework
- Google Fonts: Oswald (display, heraldic), Cormorant Garamond (editorial italic), Manrope (body), JetBrains Mono (mono)
- Unsplash imagery (replace with on-brand photography for production)
- localStorage-backed cart that persists across pages

## Design language

Italian heraldry × Fort Wayne heritage × specialty café craft. Warm cream parchment background (`#F8F2E4`), royal-navy primary surface (`#142659`), cavaliere red accent (`#DC2626`), caramel crema secondary (`#B8865D`), heraldic gold detail (`#C9A24E`). Typography pairs a condensed display sans (Oswald) with a delicate italic serif (Cormorant Garamond) — a classic heraldic-Italian pairing.

The CSS design tokens deliberately preserve the original semantic variable names (`--espresso`, `--rosso`, `--crema`, `--cream`) but rebind their *values* to Fortezza's palette. This means every component class continues to work with no per-element overrides, and a future rebrand only needs to touch the `:root` block and a few RGBA literals.

## Local preview

Open `index.html` directly in a browser, or serve with any static server:

```bash
python -m http.server 5500
# or
npx serve
```

## Deployment

Drop the contents of this folder onto:
- GitHub Pages (push to `gh-pages` or `main` with Pages enabled)
- Vercel / Netlify (zero-config — they detect static sites)
- Any web host that serves HTML

## Customization checklist (before going live)

- [ ] Replace `assets/logo.svg` with the official high-res Fortezza badge PNG (see `assets/README.md`)
- [ ] Swap stock imagery for real photos of the café, gelato case, and the Castellis
- [ ] Verify hours, prices, and menu items with Marco &amp; Sofia
- [ ] Confirm address and phone (currently demo: 215 E Berry St / (260) 422-1882)
- [ ] Hook up the contact form (Formspree / Netlify Forms / Resend)
- [ ] Add a real domain + favicon
- [ ] Confirm Instagram/Facebook handles (currently @fortezza.coffee placeholder)
- [ ] Add Google Analytics / Plausible if desired
- [ ] Wire `order.html` to Square / Toast / Clover for live ordering
