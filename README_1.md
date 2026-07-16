# ZS Pizza — Website

A single-page website for **ZS Pizza**, a pizza / burger / broast food chain based in Sector 5B, Karachi. Built as one static, dependency-free HTML file — no build step, no backend required.

🔗 **Live demo:** enable GitHub Pages on this repo (see below) and the site will be served from `index.html`.

## Features

- **Customer-facing site**
  - Hero, order-type selector (Delivery / Takeaway / Dine-in) with dynamic details
  - Tabbed menu: ZS Special, Pizzas, Burgers, Broast, Sides & Drinks
  - Add-to-order flow with a floating cart bar and order placement
  - Locations, hours, and contact section
- **Staff Portal**
  - Separate interface reached via the "Staff Portal" button in the nav
  - Demo login (see below)
  - Live order dashboard with order counts and a status pipeline: Pending → Preparing → Ready → Completed
  - Orders placed on the customer side appear in the staff dashboard in real time (client-side state)
- **Design**
  - Red / black / gray palette with a low-opacity grain texture
  - Oswald (headings), Work Sans (body), JetBrains Mono (labels/prices) via Google Fonts
  - Fully responsive, mobile nav, reduced-motion support

## Demo staff login

```
Username: staff
Password: zs1234
```

## Tech

Plain HTML, CSS, and vanilla JavaScript in a single file (`index.html`). No dependencies, no package manager, no build tools. All order/cart state lives in memory in the browser tab (it resets on page reload) — there's no backend or database wired up yet.

## Running locally

Just open `index.html` in a browser, or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — your site will be live at `https://<username>.github.io/<repo-name>/` within a minute or two.

## Next steps / known placeholders

- Menu items and prices are placeholders — update them with ZS Pizza's real menu and PKR pricing.
- The map section is a static placeholder box — swap in a real embed (e.g. Google Maps) with your exact location.
- Cart, orders, and staff login are demo-only and client-side; connecting real online ordering, payments, and staff accounts requires a backend (e.g. a small API + database), which isn't included here.

## License

MIT — see [LICENSE](LICENSE).
