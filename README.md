# PV Field Inspection

Mobile web app for solar site walkdowns: tap a subject, take a photo, pick the check, mark OK / Not OK, add notes. Records (with GPS and photos) are stored on the phone and exported as ZIP (CSV + JSON + photos).

| | |
|---|---|
| **Status** | Live |
| **Live** | https://pv-field-inspection.parrotlife.nl (old: https://midas-parrotlife.github.io/pv-field-inspection/ — until the GitHub account rename) |
| **Hosting** | Cloudflare Worker `pv-field-inspection` (static assets only) |
| **Deploy** | Automatic: push to `main` → Workers Builds runs `npx wrangler deploy` |
| **Hub** | https://parrotlife.nl |

Single file, no backend: `index.html`. Files that must not be served are listed in `.assetsignore`.

## Disclaimer

This app is a **proof of concept**, provided "as is", without warranty of any kind. You use it entirely at your own risk: to the maximum extent permitted by law, the author accepts no liability for any loss or damage, including lost data, incorrect or incomplete inspection results, missed defects, or decisions based on its records or reports. Inspection results remain the responsibility of the inspector and the asset owner; the app does not replace certified inspection procedures or safety rules. The app is **not maintained**: no support, updates or fixes, and it may stop working or go offline without notice.

## Privacy

- All inspection data (records, photos, notes, locations) is stored only in the browser on the user's device (IndexedDB). There is no server, account, database, analytics, cookie or tracker.
- Data leaves the device only when the user exports it (ZIP, CSV, photos, PDF).
- The only network request is loading `index.html` from Cloudflare, which receives the visitor's IP address, user agent and request time, like any web host. Fonts and libraries are embedded in the file, so nothing is loaded from Google or CDNs.
- Keep it that way: do not add external fonts, scripts or Cloudflare Web Analytics, or update the About text in `index.html` and this section.

## Licence

MIT, see [LICENSE](LICENSE). Embedded third-party components (JSZip, jsPDF, jsPDF-AutoTable: MIT; Barlow typeface: SIL OFL 1.1) are listed there.

