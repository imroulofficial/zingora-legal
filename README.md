# zingora-legal

Public legal and compliance website for **Zingora** by Red Pen Studio.

> This repository is **public**. It contains only the legal website. Zingora's source code,
> assets and build configuration live in a separate private repository and must never be added here.

## Contents

```
site/                         Published to GitHub Pages (this folder is the site root)
├── index.html                Landing page
├── privacy-policy.html       Privacy Policy (effective November 8, 2026)
├── terms-and-conditions.html Terms & Conditions (effective November 8, 2026)
├── support.html              Support and FAQ
├── 404.html                  Not-found page
├── app-ads.txt               AdMob authorised sellers (publisher pub-1848535996024012)
├── styles.css                Shared responsive styles (light and dark)
└── .nojekyll                 Serve files as-is
.github/workflows/pages.yml   Validate on every push/PR; deploy from main
docs/LEGAL_PAGES.md           What each page says and what is still missing
docs/DEPLOYMENT.md            How deployment works and how to enable it
```

## Status

| Item | Status |
|---|---|
| Pages and styles | Created, HTML-validated |
| Privacy Policy / Terms | **Final text**, effective November 8, 2026. No placeholders remain. The app embeds the same text (Settings > Privacy Policy / Terms) |
| app-ads.txt | Contains `google.com, pub-1848535996024012, DIRECT, f08c47fec0942fa0` |
| GitHub Pages | Needs a one-time switch-on in repository settings (see docs/DEPLOYMENT.md) |

Expected URLs once Pages is enabled and `main` is deployed:

- https://imroulofficial.github.io/zingora-legal/
- https://imroulofficial.github.io/zingora-legal/privacy-policy.html
- https://imroulofficial.github.io/zingora-legal/terms-and-conditions.html
- https://imroulofficial.github.io/zingora-legal/support.html
- https://imroulofficial.github.io/zingora-legal/app-ads.txt

**Important:** the `app-ads.txt` URL above will *not* satisfy AdMob on its own, because AdMob looks for the
file at the root of the developer website's host. The host root `https://imroulofficial.github.io/app-ads.txt`
(the Red Pen Studio user site, a separate repository) already serves the same line (checked
November 8, 2026), so set `https://imroulofficial.github.io` as the developer website in Play Console.
See docs/DEPLOYMENT.md.

**When the app changes:** the app contains a copy of `privacy-policy.html` and
`terms-and-conditions.html` (in the private game repository, `app/src/main/assets/legal/`). Update both
places in the same release so the in-app text always matches this site exactly.

## Editing

Edit the HTML files in `site/` directly. Keep the shared header, navigation and footer identical on
every page. Validate locally with:

```bash
npx --yes html-validate@10 "site/**/*.html"
```
