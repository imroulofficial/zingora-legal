# zingora-legal

Public legal and compliance website for **Zingora** by Red Pen Studio.

> This repository is **public**. It contains only the legal website. Zingora's source code,
> assets and build configuration live in a separate private repository and must never be added here.

## Contents

```
site/                         Published to GitHub Pages (this folder is the site root)
├── index.html                Landing page
├── privacy-policy.html       Privacy Policy (DRAFT)
├── terms-and-conditions.html Terms & Conditions (DRAFT)
├── support.html              Support and FAQ
├── 404.html                  Not-found page
├── app-ads.txt               AdMob authorised sellers (PLACEHOLDER)
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
| Privacy Policy / Terms | **Drafts**, with highlighted placeholders. Not final, not in effect |
| app-ads.txt | **Placeholder**, waiting for the AdMob publisher ID |
| GitHub Pages | Needs a one-time switch-on in repository settings (see docs/DEPLOYMENT.md) |

Expected URLs once Pages is enabled and `main` is deployed:

- https://imroulofficial.github.io/zingora-legal/
- https://imroulofficial.github.io/zingora-legal/privacy-policy.html
- https://imroulofficial.github.io/zingora-legal/terms-and-conditions.html
- https://imroulofficial.github.io/zingora-legal/support.html
- https://imroulofficial.github.io/zingora-legal/app-ads.txt

**Important:** the `app-ads.txt` URL above will *not* satisfy AdMob, because AdMob looks for the file at
the root of the developer website's host. See docs/DEPLOYMENT.md.

## Editing

Edit the HTML files in `site/` directly. Keep the shared header, navigation and footer identical on
every page. Validate locally with:

```bash
npx --yes html-validate@10 "site/**/*.html"
```
