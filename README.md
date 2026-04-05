# Sound Kit Tracker

QR-code based inventory management for broadcast sound kit. Built for the Ring 4 Saudi production — 68 items across Supercoms, DAZN and Terry Tew ownership.

## Features

- **QR per item** — each item gets a unique ID and QR code
- **Print labels** — print QR stickers to put on the physical kit
- **Scan in/out** — use phone camera to check gear in and out
- **Search & filter** — by category, status, owner
- **CSV import/export** — sync with Numbers/Excel
- **Offline-first** — data persists in browser localStorage

## Running locally

Just open `index.html` in any modern browser. No build step, no backend, no dependencies.

## Deploying to Railway

1. Push this repo to GitHub
2. On Railway, click **New Project → Deploy from GitHub repo**
3. Select this repo
4. Railway auto-detects the `package.json` and runs `npx serve`
5. Hit **Generate Domain** in the Settings tab to get your public URL

That's it. The `railway.json` config handles everything.

## Data storage

All inventory lives in browser localStorage on the device it's opened on. Data does **not** sync between devices automatically — use the Export CSV / Import CSV buttons to move data between a phone and a laptop.

## Notes on the Ring 4 Saudi seed data

The app pre-loads 68 items on first run (when localStorage is empty). 11 of these came through the Numbers import as "Sennheiser (TBC)" because the source file had merged cells or formatting that didn't convert cleanly — those are flagged with ⚠️ in the notes and shown in the "Needs Attention" counter. Edit each one to fill in the correct model and serial.

Hit the red **Reset** button in the header to wipe all data and reload the seed list.
