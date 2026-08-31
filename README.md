# Calculators

A small collection of free, no-signup online calculators, built as a plain static site (no framework, no build step, no dependencies).

**Live site:** https://calculator-amber-six-60.vercel.app/

## Tools

| Calculator | Path |
|---|---|
| Basic Calculator | `/calculator` |
| Simple Interest Calculator | `/simple-interest-calculator` |
| Compound Interest Calculator | `/compound-interest-calculator` |
| Age Calculator (exact age in years/months/days) | `/age-calculator` |
| Time Duration Calculator (difference between 2 dates) | `/time-duration-calculator` |

## Project structure

```
.
├── index.html                        # Landing page — links to all tools
├── calculator/index.html             # Each calculator is a self-contained folder
├── simple-interest-calculator/index.html
├── compound-interest-calculator/index.html
├── age-calculator/index.html
├── time-duration-calculator/index.html
├── assets/theme.css                  # Shared design tokens + base styles used by every page
├── robots.txt
└── sitemap.xml
```

Every calculator page is a single self-contained `index.html` (markup, styles, and vanilla JS together) that links to the shared `assets/theme.css` for design tokens. There's no build tooling — you can open any `index.html` directly in a browser and it works.

## Running locally

No install step needed. From the repo root, serve the folder with any static file server, for example:

```bash
python -m http.server 3030
```

Then open http://localhost:3030 in your browser. Clean URLs like `/age-calculator` work because each tool lives in its own folder as `index.html`.

## Using this project

Feel free to fork or copy this repo as a starting point for your own calculator/tools site. A few things to know if you do:

- **Replace the Google Analytics ID.** Every page embeds a GA4 snippet (`gtag.js`) with a measurement ID (`G-XXXXXXX...`). Swap it for your own GA4 property ID, or delete the `<!-- Google Analytics (GA4) -->` block entirely if you don't want analytics.
- **Update the canonical URLs, `robots.txt`, and `sitemap.xml`** to point at your own domain before deploying.
- **Deployment:** this site is zero-config static hosting — it's deployed on [Vercel](https://vercel.com) connected directly to the `main` branch, with no `vercel.json` needed. Any static host (Netlify, GitHub Pages, Cloudflare Pages, etc.) will work the same way since there's no server-side logic.

## License

No license file is included yet — treat this as "all rights reserved" unless a `LICENSE` file is added. Open an issue if you'd like to use this and need an explicit license.

## Disclaimer

These calculators are provided for informational purposes only. We do not take any responsibility for the accuracy of the results. Please verify results independently before relying on them.
