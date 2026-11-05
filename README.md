# SAMMPurNA – MNC Dashboards (ANC · HBNC/HBYC/PNC)

Single-file, offline-capable dashboard for Odisha NHM (Rev 82).

- Live site: https://nandiniprava1952-spec.github.io/SAMMPurNA/
- Works offline after first load; "＋ New Entry" saves on the device.
- Form language: English / ଓଡ଼ିଆ / both (selector in the form).
- Existing beneficiary search under "＋ New Entry" (ANC and HBNC): find earlier visits by name, village or mobile and pre-fill the form. Works offline.

## What's new in Rev 82
- HBNC **Visits by Designation**: the worker's designation is now read from `user_designation` (code or label text) or any other column containing "designation". Visits with a blank designation take the designation the same worker (name + district + block) has in their other visits when it clearly dominates (60%+). Only visits with no usable information stay in "Not recorded".

### Rev 81
- **Cloud repair:** if saved cloud data for a block/district is damaged ("Skipped: saved data incomplete or damaged"), saving no longer refuses. Load a file that contains those records (Load New CSV / Excel saves automatically, or click Save records to cloud) and the damaged copy is rebuilt from it. Network/server hiccups are still only retried, never overwritten.

### Rev 80
- Auto-save after **Load New CSV / Excel** made more reliable: it now waits for any cloud save/load already running (instead of failing), retries 6 times over about 5 minutes, and shows the real reason if it still cannot save. Offline-entry auto-save uses the same safe wait.

### Rev 79
- WhatsApp summary (ANC and HBNC offline entries) now has an **Address** line (village name, facility name) right below the visit date.

### Rev 78
- HBNC "＋ New Entry": **Notes** field added under Action & referral (same as ANC).
- Notes now appear in the WhatsApp summary message (ANC and HBNC).
- The "WhatsApp" section is renamed **WhatsApp (referral)** in ANC and HBNC.

### Rev 77
- HBNC tab renamed **Load New CSV / Excel**.
- After a CSV / Excel file is loaded in ANC or HBNC, its records are **saved to the cloud automatically** (merged with existing records) and the dashboard **refreshes with the updated records**. Needs a cloud login and internet; if not available yet, it waits and retries (every minute, when back online, after login).

### Rev 76
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
