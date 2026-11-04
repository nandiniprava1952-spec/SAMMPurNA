# SAMMPurNA – MNC Dashboards (ANC · HBNC/HBYC/PNC)

Single-file, offline-capable dashboard for Odisha NHM (Rev 76).

- Live site: https://nandiniprava1952-spec.github.io/SAMMPurNA/
- Works offline after first load; "＋ New Entry" saves on the device.
- Form language: English / ଓଡ଼ିଆ / both (selector in the form).
- Existing beneficiary search under "＋ New Entry" (ANC and HBNC): find earlier visits by name, village or mobile and pre-fill the form. Works offline.

## What's new in Rev 76
- Removed the "Send WhatsApp (BDM)" button and the BDM number box from Offline Records (ANC and HBNC). CSV / Excel export and Delete all are unchanged.

### Rev 75
- "＋ New Entry" (ANC and HBNC): dropdown choices (District, Block, Visit number, etc.) now always show readable text on the dark list, on phones/browsers that open a white native dropdown.

### Rev 74
- HBNC "＋ New Entry": new **Availability** field under *Child & mother* (Available / Not available / Migrated / Died / Refused).

### Rev 73
- HBNC "＋ New Entry": new **Discharged from newborn care facility (SNCU/ NBSU/NICU)** (Yes/No) field under *Birth details*. It feeds the SNCU Discharged KPI card and is saved to the cloud with the entry.

### Rev 72
- Removed the "＋ New Entry" and "Offline Records" tabs from the top bar of ANC and HBNC (the buttons on the upload card are unchanged).

### Rev 71
- HBNC **SNCU Discharged** KPI card now follows the response to *"Discharged from newborn care facility (SNCU/ NICU)"* (Yes = discharged; counted once per beneficiary; the card opens all their visits).

### Rev 70
- **Auto cloud save of offline "＋ New Entry" records**: as soon as the phone is online and a district/block/State login is active, new entries are uploaded to the cloud automatically (when the phone comes back online, when the app is reopened, and by a retry every minute). Entries always stay on the phone too. Offline (no-cloud) mode never uploads.

### Earlier (Rev 69)
- Search box under "＋ New Entry" now searches by **name / village / mobile** in both ANC and HBNC.
- Village names match in English or Odia and can be combined with a name (e.g. `Sita Badmal`).
- HBNC also searches the WhatsApp number; search results show the village.

## Update the dashboard
Replace `index.html` with the new revision and commit to `main`. GitHub Pages redeploys in ~1 minute.

## Note on offline entries
Offline entries are stored in the browser for the exact address the page is opened from. Export a CSV before switching between the downloaded file and the GitHub link.

## Do NOT commit
Raw Kobo/CSV/Excel exports or any beneficiary data (blocked by `.gitignore`).
