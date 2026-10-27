# Zain Pizza & Kebap — Ordering-first React / Tailwind prototype

A responsive, usable **front-end prototype**, not a live ordering platform.

## Quick start (Windows PowerShell)

```powershell
cd "D:\Zain_Pizza_Kebap_React"
npm install
npm run dev
```

Open the `Local:` address displayed by Vite (usually http://localhost:5173/).

Build for production (static frontend only):

```powershell
npm run build
```

## Features

- Modern cream + charcoal + tomato color system, original ZAIN concept wordmark.
- Responsive desktop cart and mobile fixed cart bar + drawer.
- Curated **36 menu entries** including published categories and publicly listed starting prices.
- Instant name/ingredient search (press `/` to focus search), sticky category pills.
- Pizza option customization panel with size/extras/notes/quantity. **All option sizes and extra prices are fictional DEMO values.**
- Basket state saved locally via `localStorage`, multiple custom item variants, quantity controls, subtotal and bottle-deposit calculation.
- Pickup / delivery selector, guest checkout UI with basic required-field validation, cash/card DEMO selection and order preview.
- German/English interface switcher (menu product titles remain German as on published menu).
- Accessible keyboard dismissals and reduced-motion support.
- Clear demo labels and official Lieferando menu link.

## Critical: before live orders

No order is actually sent. No payment is collected. This is a **product/design prototype**.

Connect an ordering backend + restaurant printer/POS, real-time store availability, delivery address/zone validation, minimum order amount and fee logic, real option pricing/ingredient/allergen and additive declarations, order tracking/cancellation, GDPR-compliant data processing and transaction email, and a compliant payment provider. Add real photos/logo only with permission from the restaurant. Replace demo item modifiers with the real menu configuration.

## Sources

The sample food names and base prices were cross-checked against the public Lieferando restaurant listing in October 2026:
https://www.lieferando.de/speisekarte/zain-pizza-kebap-76437

Published prices, hours and item availability can change.

Photos are **illustrative Unsplash-hosted stock photos**, not photos of Zain's actual meals. The website requests these via `images.unsplash.com` and requires internet to load them; in case of a broken image link the menu cards show a colored fallback. Images should be replaced with actual restaurant photography for launch.

- Margherita pizza: https://unsplash.com/photos/ and `photo-1574071318508-1cdbab80d002`
- Pizza: `photo-1565299624946-b28f40a0ae38`
- Burger: `photo-1568901346375-23c9450c58cd`
- Grill: `photo-1555939594-58d7cb561ad1`
- Pasta: `photo-1551892374-ecf8754cf8b0`
- Salad: `photo-1512621776951-a57141f2eefd`
- Fries: `photo-1573080496219-bb080dd4f877`

## Structure

- `src/menu.js` — editable product data, categories and illustrative photo URLs.
- `src/App.jsx` — visual interface + demo cart/checkout behavior.
- `src/styles.css` — Tailwind import + small custom utilities and animations.

### Notes

- Production payments and order fulfillment are intentionally **not** implemented.
- The project has a minimal `package.json` at the zip root to avoid nested extraction problems.
- Do not commit `node_modules` to Git (`.gitignore` already excludes it).
