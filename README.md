# Kadibia store

Static HTML/CSS/JavaScript storefront for **Kadibia** — seamless activewear that moves with you.

Live site: https://kadibiax7.github.io/kadibia-site-/ (GitHub Pages, served from the `/kadibia-site-/` subpath).

## How it works
- `index.html` + `app.js` build every page in the browser (shop, product, cart, FAQ, policies).
- `style.css` holds the design.
- Checkout uses Stripe Payment Links. Add each product's link in `STRIPE_LINKS` at the top of `app.js`.
- Newsletter and contact forms are sent by FormSubmit.

## Before launch checklist
- [ ] On each Stripe Payment Link, add dropdown custom fields for **Color** and **Size** so each order says which variant to buy.
- [ ] Confirm the business address in the Privacy and Terms pages is real.
- [ ] Confirm the Instagram link in the footer matches the Kadibia account.
