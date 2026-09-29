# kadibia starter store

Static HTML/CSS/JavaScript storefront. The live site is https://kadibia-store.chikadibia17.chatgpt.site/

## Upload to GitHub

Unzip this package, then upload **all extracted files and folders** to the root of your repository. GitHub does not unpack an uploaded ZIP automatically. Keep `index.html`, `style.css`, and `app.js` together.

## Preview locally

From this folder run `python3 -m http.server 8000` and open http://localhost:8000/. Opening `index.html` directly as a file may not show all routes correctly.

## Edit

- Product names, prices, images, variants and descriptions: `app.js` under `EDIT HERE`.
- Layout and colors: `style.css`.
- Header, footer, SEO description and favicon: `index.html`.
- The route folders contain copies of `index.html` so direct page visits work on a static host. If you edit `index.html`, copy it to those folders too before redeploying.

Checkout, newsletter and contact forms are demos. Connect real services and replace sample policies/reviews before taking orders.

This repository is a snapshot. Pushing to GitHub does not automatically update the existing ChatGPT Site.
