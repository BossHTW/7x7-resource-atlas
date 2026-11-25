# 7x7 Stories resource guide

Public static resource directory and youth storytelling site. No accounts or backend.

## Local preview

Run `python3 -m http.server 8000` in this directory and open `http://localhost:8000`.

## Content

- `data/resources.json` is the public source of truth. All records were researched against linked public provider pages on November 24, 2026. This is **website research, not direct provider verification**.
- Keep factual service details brief and in your own words. Preserve sources, uncertainty notes, age conditions, and `checked` dates. Updating code does not refresh the research date.
- `coordinates` come from the US Census address geocoder and are approximate. `map: false` intentionally excludes outreach, private residential, referral-only, and rotating locations from map pins. Do not geocode administrative offices as service sites.
- Never commit releases, personal contact details, raw interviews, medical information, or nomination/correction emails.
- Boss Huang’s approved third-person profile is published at `stories/boss-huang/`. Three invitation cards are open calls for future contributors; do not invent youth testimonials. Keep unpublished drafts, editorial notes, and more sensitive source material outside this public repository.

## Corrections and nominations

Recommendations, corrections, provider verification requests, and story nominations prepare a `mailto:` draft to `7x7storiessf@gmail.com`, or copy the email text. Visitors must send from their own mail app. No submission is stored by the website, and no feedback is posted automatically.

Team workflow: review incoming corrections; confirm the relevant field with the provider or a current official source; update the record and research date; describe material changes in the commit. If a report remains unresolved, flag the specific uncertainty rather than publishing a claim about an individual or replacing policy with an anecdote. Do not copy personal email content into the repository.

The map is the default view. A secondary List view includes all mapped and unmapped resources. Leaflet and provider logos are hosted locally; OpenStreetMap tiles load when the directory opens. No geolocation or advertising analytics are used. Logos identify providers; they do not imply partnership or endorsement. If a logo cannot be retrieved, a named initial badge is used. GitHub Pages and tile providers still receive ordinary connection data.

## Publishing

GitHub Pages: deploy from `main`, root directory. All links and assets are relative so project-site hosting works. `.nojekyll` bypasses Jekyll processing. No build step, API key, or paid hosting needed.

## Checks

`node --check app.js`; inspect `data/resources.json` for valid unique records and sourced locations. Manually verify filters, keyboard use, mobile layout, dialogs, copy/email behavior, map/list parity, and failure states. Test changes before publishing.

Provider verification: confirm the sender’s affiliation through an official provider address or independently sourced contact. Review fields individually before changing the public record. A submitted request alone does not verify a listing. Record any future confirmation date and scope explicitly; current listings remain website-researched.

## Assets

Brand mark reused from Boss's existing 7x7 Stories site. Leaflet 1.9.4 is distributed under its included BSD-2-Clause license. Map attribution must remain visible.

Provider logo source URLs are recorded in `assets/providers/sources.json` and each relevant resource record. Logos remain the property of their organizations. Keep all form submissions and verification correspondence out of the public repository.

When changing JavaScript, CSS, or resource data, refresh their content-version query strings (`index.html` and the data fetch in `app.js`) to avoid mixed cached versions after a Pages deploy.

Self-nominations offer a guided profile outline or a separate creative proposal. Inactive fields are disabled and excluded from the draft. Nominations for others ask for a nickname, a short reason, permission, and an optional alternative idea. All forms prepare email locally; no nomination is saved to the website. Long drafts use the copy fallback rather than risking a truncated mailto link.

Appearance: `theme.js` follows the device theme until a visitor chooses Dark mode. The choice is stored locally under `7x7-appearance` and shared by the map and story page. `theme.css` supplies both palettes. Story photos are in `assets/stories/boss/`; the published page uses only the approved public profile and selected photos.
