# 7x7 Stories resource guide

Public static resource directory and youth storytelling site. No accounts or backend.

## Local preview

Run `python3 -m http.server 8000` in this directory and open `http://localhost:8000`.

## Content

- `data/resources.json` is the public source of truth. All records were researched against linked public provider pages on November 24, 2026. This is **website research, not direct provider verification**.
- Keep factual service details brief and in your own words. Preserve sources, uncertainty notes, age conditions, and `checked` dates. Updating code does not refresh the research date.
- `coordinates` come from the US Census address geocoder and are approximate. `map: false` intentionally excludes outreach, private residential, referral-only, and rotating locations from map pins. Do not geocode administrative offices as service sites.
- Never commit releases, personal contact details, raw interviews, medical information, or nomination/correction emails.
- There are no published stories yet. The invitation is intentionally honest; do not invent youth testimonials.

## Corrections and nominations

Forms prepare a `mailto:` draft to `7x7storiessf@gmail.com`, or copy the email text. Visitors must send from their own mail app. No submission is stored by the website, and no feedback is posted automatically.

Team workflow: review incoming corrections; confirm the relevant field with the provider or a current official source; update the record and research date; describe material changes in the commit. If a report remains unresolved, flag the specific uncertainty rather than publishing a claim about an individual or replacing policy with an anecdote. Do not copy personal email content into the repository.

The map is optional. Leaflet is hosted locally; OpenStreetMap tiles load only when the map is opened. No geolocation or advertising analytics are used. GitHub Pages and tile providers still receive ordinary connection data.

## Publishing

GitHub Pages: deploy from `main`, root directory. All links and assets are relative so project-site hosting works. `.nojekyll` bypasses Jekyll processing. No build step, API key, or paid hosting needed.

## Checks

`node --check app.js`; inspect `data/resources.json` for valid unique records and sourced locations. Manually verify filters, keyboard use, mobile layout, dialogs, copy/email behavior, map/list parity, and failure states. Test changes before publishing.

## Assets

Brand mark reused from Boss's existing 7x7 Stories site. Leaflet 1.9.4 is distributed under its included BSD-2-Clause license. Map attribution must remain visible.
