# ND Fitness Co. client app

A phone app for Nico's PT business (ND Fitness Co., Redbourn Leisure Centre, Instagram @ndfitnessco).
Built by Dave Brooke for Nico. It's a separate project from NGL / SAADI.

**Live link for clients:** https://davidcbrooke.github.io/nd-fitness/ (GitHub Pages, deploys from `main`)

## How it works
- **One link.** Opened in a browser, `index.html` shows a landing page with **iPhone** and **Android** download buttons and step-by-step install instructions. Once it's added to the home screen, the dumbbell icon opens straight into the app.
- **Register on the phone.** Name, starting weight and height, goals, a PAR-Q health check and consent. At the end the client can send Nico a WhatsApp message with their sign-up details.
- **Local only.** Everything is saved on the client's phone: `localStorage` for the data, IndexedDB for progress photos. No server, no logins, no database. Nico only sees what a client chooses to send him on WhatsApp or by email (sign-up, finished workouts, weekly check-ins, booking requests).
- **Backup/restore** (Me tab) exports a JSON file. Clients need it if they change phone.
- Works offline (`sw.js`). **Bump `VERSION` in `sw.js` every time you change a file**, otherwise phones keep the old copy.

## Features
Home (week strip, next workout, habits, next bootcamp class, tip) · Train (5 programmes, Hevy-style workout logger with previous sets, rest timer, PBs, 45-exercise library with coaching cues) · Progress (weight chart in kg or stone, measurements, photos, weekly volume, PBs) · Nico (contact, booking, check-in, bootcamp prices, about, qualifications, reviews) · Me (profile, health check, units, backup, delete).

## Edit Nico's details
All of Nico's details live in the `NICO` object at the top of the script in `index.html`: phone, email, class times, prices, about text, qualifications and reviews. The programmes are in `PROGS` and the exercises in `EX_RAW`.

**Check with Nico:** the bootcamp prices (£225 1:1, £275 2:1) and class times (Mon 08:30, Tue 11:45, Wed 19:30, Fri 12:30) come from his April 2026 Instagram flyer.

## Run locally
`python -m http.server 8791` in this folder, then open http://127.0.0.1:8791

## Files
- `index.html`: the whole app (landing page, registration, app)
- `manifest.webmanifest`, `sw.js`: install and offline support
- `assets/`: logo, dumbbell icon, app icons, Bebas Neue font
- `brand/`: Nico's original Instagram screenshots (logo, reviews, price flyer)
- `docs/`: preview screenshots
