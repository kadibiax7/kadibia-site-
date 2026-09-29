# Upload this to GitHub (about 2 minutes)

This puts your selected product live: the **Seamless Push-Up Leggings** ($31.00, Women's category) with a real product photo, and the 8 template samples stay hidden so the shop shows only your real product.

## Steps

1. Go to https://github.com/kadibiax7/kadibia-site-
2. Click **Add file → Upload files**
3. Drag in **everything** from the `for-github-upload` folder in this zip
   (new/changed: `app.js`, new folder `product/seamless-push-up-leggings/`, new folder `images/`)
4. Click **Commit changes**
5. Wait ~1 minute, then open https://kadibiax7.github.io/kadibia-site-/shop — the Seamless Push-Up Leggings should be the only product, with a NEW badge.

## After uploading — to take real payments (free, ~10 min)

The "Buy now" button won't work until you connect Stripe:

1. Create a free account at https://stripe.com
2. Go to **Payments → Payment Links → Create payment link**
3. Name: `Seamless Push-Up Leggings`, price: **$31.00 USD**, copy the link (looks like `https://buy.stripe.com/abc123...`)
4. Open `app.js`, find the line `'seamless-push-up-leggings': 'https://buy.stripe.com/REPLACE_ME_seamless-push-up-leggings'` and paste your real link over the placeholder
5. Re-upload just `app.js` to GitHub — done, the Buy button works

## Product & pricing notes

- Supplier: https://www.aliexpress.us/item/3256805822806589.html (PranaFlow Apparel Store, 4.5★, 455 reviews, 4,000+ sold)
- Supplier cost: **$19.14** regular — the $3.38 "welcome deal" is one-time only (max 1 per shopper), so count on $19.14
- Your price **$31.00** leaves ~$10.66 per order after Stripe's fee (~$1.20)
- Colors and sizes on the site: Brown, Black, Navy, Gray, Light Gray / XS, S, M, L — double-check these against the listing's exact variant names before fulfilling orders
- Free shipping from the supplier; delivery shown as Oct 04–12
- When a customer buys, you place the same order on the AliExpress listing and the supplier ships it to them. You never touch the product.
