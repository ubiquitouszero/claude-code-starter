# State

**Last updated:** 2026-04-15

## What I'm working on

Adding a "Travels" page with photos from the trip to St. Simons. Photos are in `images/st-simons/` (12 of them, all from my phone, not yet compressed).

## Where I left off

- Drafted `travels.html` with a photo grid layout. Looks OK on desktop.
- Mobile is broken — photos overflow the viewport.
- Started a CSS media query but haven't tested it yet.

## Decisions in flight

- Whether to add a lightbox for clicking on photos. Leaning yes but the vanilla JS for it looked annoying. Maybe just bigger thumbnails for now.
- Whether to put photos in a folder per trip (`images/st-simons/`) or one big `images/travels/` folder. Currently per-trip. Decide before adding the next trip.

## Things to remember

- Photos haven't been compressed yet. Run them through TinyPNG (or ask Claude to use ImageMagick) before pushing or the site will be slow.
- Netlify deploy is still manual — drag the folder into the dashboard. Need to remember to deploy after committing.
