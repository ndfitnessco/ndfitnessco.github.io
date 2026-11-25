# ND Fitness app: handover

## Status (25 Nov 2026)
- **Built and live:** https://ndfitnessco.github.io (GitHub organisation `ndfitnessco`, owned by Dave; repo `ndfitnessco/ndfitnessco.github.io`).
- **Waiting on Nico to review it.** Dave has sent it, or is about to send it, to Nico. Don't send the link to clients until Nico has signed it off.

## Once Nico has reviewed: checklist
Ask Nico about each item. Make the change in `index.html` (his details are in the `NICO` object at the top of the script), bump `VERSION` in `sw.js`, then commit and push. The site updates itself, and clients get the new version the next time they open the app.

1. **Prices.** 6-week bootcamp £225 (1:1) and £275 (2:1). These come from his April 2026 Instagram flyer. Are they still right? Does he want other prices shown (single PT session, packages, taster)?
2. **Bootcamp class times.** Mon 08:30, Tue 11:45, Wed 19:30, Fri 12:30, from the same flyer. Still running? The Home screen shows "Next bootcamp class" from these.
3. **Contact details.** Mobile 07485 074661, email Contact@NdfitnessCo.com, Instagram @ndfitnessco. WhatsApp sign-ups, check-ins, workouts and bookings all go to that mobile.
4. **About text, qualifications and reviews (Vicky, Emma, Elaine).** All taken from his flyer and Instagram stories. Is he happy for them to be used, and does he want to add or change any?
5. **Programmes.** Five plans: 6-Week Bootcamp, Fat Loss Starter, Build Muscle, Lower Back Care, No-Kit Home. Does he want to change exercises, sets or reps, or add his own plans? They're in `PROGS` in `index.html`, and the exercises are in `EX_RAW`.
6. **Photo of Nico.** There isn't one in the app yet. A clear portrait would go well on the Nico tab.
7. **Own address (optional).** If he wants `app.ndfitnessco.com`, he adds one DNS record in his Squarespace account: CNAME, host `app`, data `ndfitnessco.github.io`. Then set the custom domain on GitHub Pages (repo Settings → Pages) and turn on HTTPS. Dave doesn't have access to his Squarespace.
8. **Anything else** he asks for: list it here, then build it.

## How the app works (for whoever picks this up)
See `README.md`. In short: one HTML file, installable on iPhone and Android, all client data kept on the client's phone (no server). Clients send things to Nico on WhatsApp or by email.

## Log
- **25 Nov 2026:** Built and tested. Published first at davidcbrooke.github.io/nd-fitness, then moved to the `ndfitnessco` organisation so Dave's GitHub name isn't in the link. The old link no longer works.
