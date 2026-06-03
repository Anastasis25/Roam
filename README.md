# Roam

Animated journey visualiser for Luxe Sailing — sailing, land, and art tours.

Roam turns an itinerary into a cinematic route film: a vessel traces the path
across a real map of the region, with live distances and a leg-by-leg timeline.
"View in Roam" / "Share your Roam".

## What it does
- Draws the route over real coastline data (baked in — nothing is fetched at runtime).
- Imports an itinerary in the shape the TMS returns (`legs[]` with `lat`/`lng`, `nights`, `code`).
- Animates the journey with pause/resume and adjustable speed.
- Shows nautical distance per leg and total, plus a live progress bar.
- Three on-brand palettes: Navy, Night, Ivory.

## Run it
It's a single self-contained file. Open `index.html` in any browser, or host the
folder on any static host (GitHub Pages, Netlify, Cloudflare Pages).

## Wiring to the TMS
Replace the hardcoded `TMS_BOOKING` object with a `fetch()` to the TMS endpoint.
The only fields Roam needs per leg are `destination`, `lat`, `lng`; `nights` and
`code` enrich the panel. Any leg missing coordinates is where geocoding fills in.
