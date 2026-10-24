# Rafiq Engineering Works

Official static website and brand assets for Rafiq Engineering Works, a fabrication workshop in Nambal, Anantnag, Jammu & Kashmir.

The website is plain HTML/CSS/JavaScript. It has no build step and is deployed automatically to GitHub Pages by GitHub Actions whenever changes are pushed to `main`.

## GitHub Pages

After the repository is created, open **Settings → Pages** and choose **GitHub Actions** as the build and deployment source. The workflow in `.github/workflows/deploy.yml` will upload the repository root and publish `index.html`.

Expected project-site URL:

`https://mahidrafiq.github.io/rafiq-engineering-works/`

The first deployment may take a few minutes. View the **Actions** tab to confirm that “Deploy Rafiq Engineering Works to GitHub Pages” completed successfully.

## Contact details

Phone and WhatsApp numbers are configured in the `CONFIG` object near the bottom of `index.html` (`whatsapp`, `phone`, `phone2`, `phone3`, and `email`). Verify these details before public promotion.

## Indicative prices (optional)

The design tool calculates area in square feet. To display indicative prices, set per-square-foot rates in `CONFIG.rates`, for example:

```js
rates: { gate: 450, grill: 300, shutter: 350 }
```

Keep values at `0` to hide prices.

## Add photos of completed work

Put images in `img/work/` and list them in `CONFIG.photos`, for example:

```js
photos: [
  { src: "img/work/gate-1.jpg", caption: "Two-leaf gate, Anantnag", type: "Gates" },
  { src: "img/work/grill-1.jpg", caption: "Window grills", type: "Grills" }
]
```

Keep image paths relative (such as `img/work/gate-1.jpg`) so they work under the GitHub Pages project URL.

## Innovations catalogue

The `CONFIG.innovations` array in `index.html` lists tools, prototypes and engineering ideas. Use accurate availability descriptions. Add product photos under `img/products/`; the site provides an illustration fallback when a photo is not configured or available.

## Run locally

From the repository root:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Brand assets

The `brand/` folder contains logo exports, the approved identity board, application concepts and brand guide. Treat the final identity board as the visual master; do not redraw the monogram independently.

## Deployment notes

- Static-only hosting: no server runtime or secrets are needed.
- Relative asset URLs are required for GitHub Pages subpaths.
- GitHub Pages deployment is handled by GitHub Actions in `.github/workflows/deploy.yml`.
- This is a static brochure/catalogue site. The quote flow uses phone/WhatsApp handoff; it does not store submissions in a database.
