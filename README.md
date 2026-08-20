# Refsol Marketing — Website

Static, self-contained two-page site: `index.html` (home) and `products.html` (product catalog).

## Structure
```
index.html          Home page (hero, about, gallery, contact)
products.html       Product catalog with detail panel
scripts/
  support.js        Client-side rendering runtime (loads React/Babel from CDN at runtime)
  image-slot.js      Image placeholder/drop component used on both pages
assets/
  refsol-logo.png    Site logo
uploads/             Product & team photos referenced by both pages
```

No build step — these are plain static files. `support.js` fetches React/ReactDOM/Babel from a public CDN (unpkg) the first time the page loads, so the site needs an internet connection but no server-side code or database.

## Deploy on GitHub Pages
1. Push this folder's contents to the root of a GitHub repo (or to a `docs/` folder / `gh-pages` branch — whatever you point Pages at).
2. In the repo: **Settings → Pages → Source**, pick the branch/folder containing these files.
3. GitHub serves `index.html` at the repo's Pages URL automatically; `products.html` is reachable via the in-page nav links.

## Deploy anywhere else
Any static host works (Netlify, Vercel static, S3, nginx, etc.) — just upload this folder as-is, keeping the folder structure intact (scripts/, assets/, uploads/ must stay alongside the two HTML files).
