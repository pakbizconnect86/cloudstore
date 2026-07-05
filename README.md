# CloudStore — Premium Earbuds Store

A fully responsive, static eCommerce front-end (no build step, no backend) inspired by "Cloud Store". Pure HTML, CSS and vanilla JavaScript.

## Structure
```
cloudstore/
├── index.html         Home page — hero, catalog, filters, search, modal, cart drawer
├── checkout.html      Checkout page — shipping form, payment method, order summary
├── contact.html       Contact page — info + message form
├── css/
│   └── style.css      Design tokens, glassmorphism, dark/light theme, responsive rules
├── js/
│   ├── data.js         Product catalog (edit here to add/remove products)
│   ├── cart.js         Cart + wishlist state (localStorage-backed)
│   ├── main.js          Home page interactions
│   ├── checkout.js      Checkout page interactions
│   └── contact.js       Contact page interactions
└── images/             Product SVG illustrations
```

## Run it
No build tools needed. Just open `index.html` in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server
```

## Notes
- Cart and wishlist persist via `localStorage`, so they survive a page refresh or navigating between pages.
- Dark mode is the default; toggle to light from the nav pill switch.
- All product images are hand-built inline SVGs — swap the files in `images/` for real photography whenever you have it.
- Checkout and the newsletter/contact forms are front-end only (no server) — wire the `submit` handlers in `js/checkout.js` and `js/contact.js` to your backend or a form service (e.g. Formspree) when ready.
- To add a product: add an entry to `PRODUCTS` in `js/data.js` — it will automatically show up in the grid, search, and filters.
