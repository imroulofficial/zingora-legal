# Deployment

## How it works

`.github/workflows/pages.yml`:

- **Every push and pull request:** checks that the required files exist, validates all HTML with
  `html-validate`, checks internal links, and refuses source code or keystores in `site/`.
- **Pushes to `main` only:** uploads `site/` and deploys it with the official
  `actions/deploy-pages` action.

## One-time setup (repository owner)

GitHub Pages must be switched on once. The workflow's built-in token is not allowed to do this.

1. Open https://github.com/imroulofficial/zingora-legal/settings/pages
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Merge the setup pull request into `main` (or re-run the latest **Legal site** workflow on `main`).
4. When the **Deploy to GitHub Pages** job is green, the site is live at
   https://imroulofficial.github.io/zingora-legal/

## app-ads.txt and AdMob

AdMob's crawler reads the **developer website** from the Google Play listing and looks for
`app-ads.txt` at the **root of that host** (it ignores `www.` and `m.`, and probes at most one
subdomain level). Sources:
[Set up app-ads.txt](https://support.google.com/admob/answer/9363762),
[Ensure app-ads.txt can be crawled](https://support.google.com/admob/answer/9679128),
[Ad Manager: host ads.txt/app-ads.txt](https://support.google.com/admanager/answer/9422161).

This project site serves the file at `https://imroulofficial.github.io/zingora-legal/app-ads.txt`.
That is a sub-path, not the root of a host, so **AdMob verification is not expected to work with it**.

**Status (checked November 8, 2026):** the Red Pen Studio user site already serves
`https://imroulofficial.github.io/app-ads.txt` with exactly
`google.com, pub-1848535996024012, DIRECT, f08c47fec0942fa0`, so option 2 below is in place. Use
`https://imroulofficial.github.io` as the developer website in the Play listing. The copy in this
repository (`site/app-ads.txt`) holds the same line for reference.

The two options were:

1. **Custom domain (recommended).** Register a domain (for example a Red Pen Studio domain), point it
   at this Pages site in **Settings → Pages → Custom domain**, and use it as the Play developer website.
   `app-ads.txt` in `site/` is then served at `https://<your-domain>/app-ads.txt`.
2. **GitHub user site.** A separate public repository named `imroulofficial.github.io` serves from the
   host root `https://imroulofficial.github.io/`. `github.io` is on the Public Suffix List, so that host
   is treated as its own root domain. The developer website in Play would then be
   `https://imroulofficial.github.io`. This adds a second public repository.

AdMob also only verifies after the app is published on Google Play with the developer website set.
