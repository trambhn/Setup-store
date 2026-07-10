# LitCommerce Onboarding Mockup

Interactive, high-fidelity mockup of the LitCommerce 2-step onboarding flow:
**Step 1 — Setup Main Store** and **Step 2 — Setup First Channel**.

A single self-contained `index.html` — no build step, no dependencies to install.
Open it directly in a browser, or serve it with GitHub Pages (see below).

## What's inside
- `index.html` — the full interactive mockup (React, precompiled to plain JS —
  no in-browser Babel transformer, no external UI library).
- `create-repo.sh` — helper script used to publish this project to GitHub.

## What it demonstrates
- **Step 1 (Setup Main Store):** compact, description-free platform cards
  (Shopify, Wix, WooCommerce, Squarespace, BigCommerce, Square) plus file
  import options (CSV / Google Sheet). Clicking a card goes straight to a
  mock "Connect / Authorize" screen — no separate Connect button. A "Skip —
  I don't have any of these" option moves straight to Step 2.
- **Step 2 (Setup First Channel):** the same compact card pattern for
  Marketplaces (TikTok Shop, Amazon, eBay, Etsy, Walmart, Walmart Canada,
  Facebook Shop, Google Merchant, Reverb, Shopee, Temu, Faire) and Shopping
  Carts. Includes a clear "Restart Setup" flow (with a redesigned
  confirmation modal) for changing your mind about the Main Store.
- **Breadcrumb:** a display-only 2-step progress indicator (Setup Main Store
  → Setup First Channel). It is intentionally **not clickable** — steps
  can't be skipped ahead to or revisited by clicking, matching the real
  product's constraint.

## Run it
Just open `index.html` in any browser — double-click it, or drag it into a
browser tab. Nothing to install.

## Publish to GitHub Pages
Once pushed to GitHub (see below), go to **Settings → Pages → Source:
`main` / root** in the repo to get a live URL at
`https://<your-username>.github.io/<repo-name>/`.

## Publishing this repo
This folder includes `create-repo.sh` to automate creating the GitHub repo
and pushing this code.

```bash
# Auth: run `gh auth login` once, OR export GITHUB_TOKEN=<token with 'repo' scope>
cd litcommerce-onboarding-mockup
chmod +x create-repo.sh
./create-repo.sh litcommerce-onboarding-mockup public "Interactive LitCommerce onboarding mockup"
```

This will initialize git, commit the files, create the GitHub repository,
and push to `main`.
