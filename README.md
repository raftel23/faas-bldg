# FAAS Building Appraisal Guide (PWA)

A standalone, lightweight, mobile-first Progressive Web App (PWA) prototype for Philippine Local Government Unit (LGU) Field Appraisal & Assessment Sheets (FAAS) for Buildings.

## Features
- **Offline-First Storage**: Powered by IndexedDB via Dexie.js for persistent, non-blocking local storage on mobile devices.
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
  - Assessed Value applies `roundNearest10(Total Building Cost) * Assessment Level %`, with the final assessed value rounded to the nearest 10.
