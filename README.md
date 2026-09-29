# Kadibia store

Static HTML/CSS/JavaScript storefront for **Kadibia** — quality goods for family life.
Live site: https://kadibiax7.github.io/kadibia-site-/ (GitHub Pages, served from the `/kadibia-site-/` subpath).

## Upload to GitHub

Unzip the package, open the `for-github-upload` folder, select **everything inside it**,
then on the repo page: **Add file → Upload files** → drag them in → commit.
GitHub does not unpack an uploaded ZIP automatically.

## Preview locally

From the `for-github-upload` folder, serve it under the `/kadibia-site-/` base path:

```bash
mkdir -p /tmp/sitetest && ln -sfn "$PWD" /tmp/sitetest/kadibia-site-
cd /tmp/sitetest && python3 -m http.server 8123
```

Then open http://localhost:8123/kadibia-site-/ — every route, the cart, and checkout
work there exactly as on GitHub Pages.

## Edit

- **Products**: `app.js` — the catalog under `EDIT HERE` (schema documented in the comments).
- **Payments**: `app.js` — `STRIPE_LINKS` at the top maps each product id to its Stripe Payment Link (see STEP 1 comment).
- **Layout and colors**: `style.css`.
- **Header/footer shell**: `index.html` — after editing, copy it into every route folder (`about/`, `cart/`, `checkout/`, `contact/`, `faq/`, `privacy/`, `shipping-returns/`, `shop/`, `terms/`, `product/*/`) so direct page visits work on a static host.

## Before taking real orders

See `UPLOAD_AND_SETUP.md` (in the zip root) for the setup checklist: Stripe Payment Links,
newsletter/contact form endpoints, `[TO FILL]` policy details, and swapping in real products.
