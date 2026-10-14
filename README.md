# FAAS Building Appraisal Guide (Offline PWA)

A standalone, lightweight, mobile-first Progressive Web App (PWA) prototype for Philippine Local Government Unit (LGU) Field Appraisal & Assessment Sheets (FAAS) for Buildings.

## 📱 PWA & 100% Offline Ready
- **Installable Web App**: Includes a `manifest.json` and PWA service worker (`sw.js`). Users can install it directly to their home screen on Android, iOS, or desktop.
- **Zero External Dependencies**: Bundles `dexie.min.js` locally inside the project—no CDN connection required.
- **Persistent IndexedDB**: Works completely offline in areas without internet connectivity.

## Features
- **Master List & Live Search**: Instant multi-field search (Owner Name, Lot & Block, Address, Building Type) and sorting (Latest to Oldest, Oldest to Latest, Name A-Z).
- **Building Valuation**:
  - Building Type selection: **Residential** or **Commercial**.
  - Multi-floor support with separate area inputs per floor automatically summed into Total Building Floor Area.
  - Core building cost subtotal computation.
- **Dynamic Appurtenances**: Dynamic sub-item entries for Porch, Terrace, Balcony, Car Port (with 30%/40% toggle rates), and Tiles.
- **Progressive Assessment Level Schedule**:
  - Automatically suggested assessment level percentages based on Total Building Cost brackets for Residential and Commercial types.
  - Fully editable for manual override with an auto-fill reset option.
- **Precise Rounding**:
  - Core, additional items, and total costs remain exact and unrounded.
  - Assessed Value applies `roundNearest10(Total Building Cost * Assessment Level %)`, rounding only at the final Assessed Value.

## How to Install as an App
1. **GitHub Pages / HTTPS Hosting**:
   - Enable GitHub Pages in your repo settings (`Settings` -> `Pages` -> Source: `main` branch, `/ (root)`).
2. **On Mobile (Chrome / Android)**:
   - Visit the site URL, tap the browser menu (⋮) -> **"Install app"** or **"Add to Home Screen"** (or tap the **"📲 Install FAAS App to Home Screen"** prompt).
3. **On iOS (Safari)**:
   - Tap the Share button -> **"Add to Home Screen"**.
