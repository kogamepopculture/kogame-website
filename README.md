# KOGAME static website

This folder is ready to publish on GitHub Pages.

## Files
- `index.html` — website
- `styles.css` — design / responsive layout
- `script.js` — mobile menu + current year
- `assets/kogame-logo.png` — KOGAME logo
- `assets/favicon.png` — Westie favicon
- `.nojekyll` — tells GitHub Pages to serve the site as plain static files

## Publish on GitHub Pages

1. Create a GitHub account if you do not already have one.
2. Create a new **public** repository, for example `kogame-site`.
3. Upload all files from this folder (keep the `assets` folder).
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
6. Save. GitHub will give you a temporary `github.io` address.

## Connect `kogame.ie`

In GitHub:
1. Settings → Pages → **Custom domain**
2. Enter `kogame.ie`
3. Save.

In GoDaddy DNS, add the GitHub Pages records shown in GitHub's documentation.
For the apex/root domain, GitHub currently uses A records for its Pages servers.
For `www`, create a CNAME pointing to your GitHub Pages hostname.

After DNS has propagated, enable **Enforce HTTPS** in GitHub Pages.

## Easy product updates

Search `index.html` for `<article class="product-card">`.
Each product card contains:
- image URL
- item name
- price
- Adverts.ie link

Duplicate a card to add a new item, or replace its details.

## Notes

The current featured product images are loaded from the same Wix-hosted image URLs used by your existing site.
If you later delete those Wix-hosted images, copy the product photos into this site's `assets` folder and replace the image URLs with local file names.
