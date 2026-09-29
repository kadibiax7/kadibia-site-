# Kadibia site — upload & setup guide

This zip contains the full "content pass" update for the Kadibia store:
real brand copy, honest policies, Stripe Payment Links checkout, and
wired-up newsletter/contact forms.

## Part 1 — Upload (about 3 minutes)

1. Unzip this file on your computer.
2. Open the `for-github-upload` folder and **select everything inside it**
   (all files and folders — NOT the folder itself).
3. Go to https://github.com/kadibiax7/kadibia-site-
4. Click **Add file → Upload files**.
5. Drag everything in, scroll down, click **Commit changes**.
6. Wait 2–5 minutes, then open https://kadibiax7.github.io/kadibia-site-/
   and confirm the homepage loads with styling.

## Part 2 — Setup checklist (do these before taking real orders)

### 1. Take payments with Stripe — FREE, no monthly fee (~10 min)
Stripe only charges ~2.9% + 30¢ when someone actually buys. Nothing upfront.
1. Create a free account at https://stripe.com
2. Dashboard → **Payments → Payment Links → Create payment link**
3. Make **one link per product**: set the product name + price in USD.
   (Optional: add your flat shipping rate inside the link settings.)
4. Copy each link URL (looks like `https://buy.stripe.com/abc123...`).
5. Open `app.js`, find `STRIPE_LINKS` at the very top, and paste each URL
   over its `REPLACE_ME_...` placeholder. Full step-by-step is in the
   comment right above it.
6. Re-upload just `app.js` to GitHub (same Add file → Upload files flow).

### 2. Newsletter signup — FREE
The footer + homepage signup forms are pre-wired. Pick one:
- **Mailchimp (free tier):** Audience → Signup forms → Embedded forms →
  copy the form's `action` URL → paste it into the `action="..."` of both
  newsletter `<form>` tags (one in `index.html`, one in `app.js`).
- **Formspree:** https://formspree.io → new form → paste your
  `https://formspree.io/f/xxxx` endpoint into the same `action` attributes.
Until you paste a real URL, the forms politely say "not connected yet".

### 3. Contact form — FREE
Same deal: create a free form at https://formspree.io and paste your
endpoint URL into the `action="..."` of the contact `<form>` in `app.js`.
Instructions are in the HTML comment right above the form.

### 4. Fill in your business details — search for `[TO FILL]`
Open `app.js` and search for `[TO FILL]`. You'll find spots in the
shipping & returns, privacy policy, and terms of service pages for:
- your legal business name
- support email + privacy email
- flat shipping rate for orders under $75 (e.g. 6.95)
- your state (for governing law)
- the "last updated" dates

### 5. Replace the contact email placeholder
Search for `hello@example.com` (contact page in `app.js`) — it's flagged
with `<!-- REPLACE: your contact email -->`. Put your real support email.

### 6. Instagram link
Footer in `index.html` has `https://instagram.com/REPLACE_ME` flagged with
`<!-- REPLACE: your Instagram profile URL -->`.

### 7. Swap in your real products (when picked)
In `app.js`, the catalog under `EDIT HERE` documents the exact product
format. For each real product: replace the sample entry, create its Stripe
Payment Link (step 1), and if you add/rename products, copy a
`/product/<id>/` folder to the new id so the page works when visited
directly. Delete any product folders you're not using.

## What's already done for you

- Warm Kadibia brand copy on homepage, About, FAQ — no lorem ipsum left
- Honest shipping & returns, privacy policy, and terms of service pages
  for a US dropship / print-on-demand store (7–15 business day delivery,
  30-day returns, made-to-order final-sale rule)
- Fake testimonials and fake star ratings removed
- Checkout rebuilt around Stripe Payment Links — no backend needed
- Cart keeps working for browsing; checkout shows per-item Buy now buttons
- All page paths still use the `/kadibia-site-/` prefix GitHub Pages needs
