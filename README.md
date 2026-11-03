# SAMMPurNA – MNC Dashboards (ANC · HBNC/HBYC/PNC)

Single-file, offline-capable dashboard for Odisha NHM (Rev 69).

- Live site: https://nandiniprava1952-spec.github.io/SAMMPurNA/
- Works offline after first load; "＋ New Entry" saves on the device.
- Form language: English / ଓଡ଼ିଆ / both (selector in the form).
- Existing beneficiary search under "＋ New Entry" (ANC and HBNC): find earlier visits by name, village or mobile and pre-fill the form. Works offline.

## What's new in Rev 69
- Search box under "＋ New Entry" now searches by **name / village / mobile** in both ANC and HBNC.
- Village names match in English or Odia and can be combined with a name (e.g. `Sita Badmal`).
- HBNC also searches the WhatsApp number; search results show the village.

## Update the dashboard
Replace `index.html` with the new revision and commit to `main`. GitHub Pages redeploys in ~1 minute.

## Note on offline entries
Offline entries are stored in the browser for the exact address the page is opened from. Export a CSV before switching between the downloaded file and the GitHub link.

## Do NOT commit
Raw Kobo/CSV/Excel exports or any beneficiary data (blocked by `.gitignore`).
