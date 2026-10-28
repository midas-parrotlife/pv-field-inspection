# PV Field Inspection

Mobile web app for solar site walkdowns: tap a subject, take a photo, pick the check, mark OK / Not OK, add notes. Records (with GPS and photos) are stored on the phone and exported as ZIP (CSV + JSON + photos).

| | |
|---|---|
| **Status** | Live |
| **Live** | https://pv.parrotlife.nl (old: https://midas-parrotlife.github.io/pv-field-inspection/ — until the GitHub account rename) |
| **Hosting** | Cloudflare Worker `pv-field-inspection` (static assets only) |
| **Deploy** | Automatic: push to `main` → Workers Builds runs `npx wrangler deploy` |
| **Hub** | https://parrotlife.nl |

Single file, no backend: `index.html`. Files that must not be served are listed in `.assetsignore`.
