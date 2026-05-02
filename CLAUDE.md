# MacroCoats Brochure — CLAUDE.md

## Project Overview

A 4-page A4 print brochure (`brochure.html`) for **Macro Coats Pvt. Ltd.** (formerly Technical Electroless Chemical Co. Pvt. Ltd., est. 1993). The brochure is a single self-contained HTML file with embedded CSS — no build step, no dependencies beyond Google Fonts.

## File Structure

```
brochure/
└── brochure.html   # Single file — all HTML, CSS, and inline SVG
```

## Brand Identity

| Token | Value |
|---|---|
| Primary (Indigo) | `#2D2A8C` |
| Accent (Magenta) | `#8B2C7D` |
| Magenta soft | `#B254A6` |
| Graphite body | `#3A3F4B` |
| Off-white bg | `#F8F7F4` |
| Font | Inter (Google Fonts), weights 400/500/600/700/800 |

## Page Layout

All pages are `210mm × 297mm` (A4), rendered as `.page` blocks stacked in a `.pages` flex column. Print media query removes shadows and adds `page-break-after: always`.

| Page | Content |
|---|---|
| 1 — Cover | Hero image with indigo/magenta overlay, logo lockup, tagline |
| 2 — Who We Are | Stats strip (1993 / 30+ yrs / 7 industries / 100% custom), 3×2 capability cards, industrial applications strip |
| 3 — Product Portfolio | 5 categories / 16 products in card grid, Industrial Oils & Process Fluids section |
| 4 — Clients + Why Choose + Contact | 6 client logos, 4 why-choose cards, closing band, footer with QR placeholder |

## Product Catalogue

**Primary (phosphating)**
- Iron Phosphating — 5 products (UNI-IRON PHOSPHATE, UNIKCONDITIONER, UNIKTONNER, UNIKLEAN SP, UNIPASS-FE)
- Zinc Phosphating — 4 products (UNIKOAT LT450 Hot, UNIKOAT LT700/LT450 RT, UNIKOAT LT2000, UNIKLEAN 3 IN 1)
- Manganese Phosphating — 1 product (UNI-MANGANESE PHOS, up to 30 g/m²)

**Supporting**
- Aluminium Treatment — 4 products (UNIKLEAN-AL, UNIPASS-AL CHROME, UNIPASS-AL NON CHROME, UNIPASS-AL)
- De-Rusting — 2 products (UNISOLVE H3, UNISOLVE)

**Extended portfolio (oils)**
Rust Preventive Oils · Industrial Lubricants · Duncan Oil · Coolants · Cutting Oils · Dewatering Fluids

## Key Clients

Indian Railways, TVS Motor Company, Larsen & Toubro, Rane Group, Chemplast Sanmar, Tube Investments of India

## Contact

- Company: Macro Coats Pvt. Ltd., Chennai, Tamil Nadu, India
- Phone: +91 98840 80377
- Email: info@macrocoats.in
- Website: macrocoats.in

## Design Notes

- All icons are inline SVG (no icon library dependency)
- Client logos pull from Wikimedia Commons URLs — replace with local assets for offline/print use
- Hero image on cover page uses `filter: saturate(0.55) hue-rotate(205deg) brightness(0.78)` to align with the indigo palette
- The QR placeholder (`.qr-ph`) needs a real QR image before final print
- `@media print` collapses page gaps and removes box shadows
