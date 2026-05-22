# TurfVision by Iris — Website

A six-page website for Turf-Vision.ca, built around the May 2026 brief.

## Files

| File | Page |
|---|---|
| `index.html` | Home — hero, problem, four-step flow, request form |
| `product.html` | Product detail — Alert vs Shutdown, specs, compatibility, pricing |
| `why-greens.html` | The greens-specific cost story + ROI calculator |
| `platform.html` | The three-product Iris arc |
| `dealers.html` | Dealer program + dealer application form |
| `about.html` | Mission, technology, contact |
| `styles.css` | Shared stylesheet for all pages |

## Design system

- **Palette:** Deep instrument blacks (`#0a0d0c`, `#11161a`) with IR thermal accents — electric teal (`#1fd1c1`) as the baseline scan color, warm amber (`#ffa024`) as the anomaly/detection color
- **Typography:** Space Mono (instrument-panel labels, eyebrows, tags) paired with Inter Tight (headlines and body)
- **Motifs:** Aperture/crosshair imagery throughout, scanline overlays, thermal-gradient hero, blinking status indicators

The hero on the homepage includes an animated thermal aperture visualization (pure CSS, no images required) showing an active scan with a pulsing amber anomaly — communicates the product instantly without needing the 60-second video yet.

## What needs to be added before going live

1. **The 60-second IR detection video** — the brief identifies this as the #1 priority asset. It should be added to the homepage hero (replacing or supplementing the CSS thermal visualization) and the product page
2. **Real product photography** — the device mounted on a mower, scanning a fairway
3. **Form backend** — the Request Info form (homepage) and Dealer Application form (dealers page) currently show a success state on submit. Wire them to Formspree, a Google Sheets endpoint, or a CRM (HubSpot, Salesforce, etc.). The forms are already structured with named fields ready to POST
4. **Real superintendent testimonials** post-beta (placeholder is already on the homepage)
5. **Real dealer locator** if it becomes a feature in V2 — the current "Find a Dealer" path is the Request Info form, which is appropriate for launch
6. **Privacy / Terms / Patents pages** — footer links are stubs (`#`)
7. **Update contact email** — `about.html` references `hello@turf-vision.ca` as a placeholder

## Deployment

Single-folder static site. Drop these files into the root of `Turf-Vision.ca` via whatever host the domain points at (Cloudflare Pages, Netlify, GitHub Pages, traditional hosting). No build step. No dependencies beyond Google Fonts (loaded via CDN).

## Brand note

Built as "TurfVision by Iris" so it works at `Turf-Vision.ca` today and can slot into a future `iristurf.com` parent without rework. Iris is the company; TurfVision is the product. The nav brand reads `IRIS / TURFVISION` throughout.
