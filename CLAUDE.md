# CLAUDE.md — pv-field-inspection

- Single-file app: everything lives in `index.html`. Keep it dependency-free and working offline on a phone.
- Deploy is automatic on push to `main` (Cloudflare Workers Builds). Never deploy by hand.
- Anything added to the repo root is served publicly unless listed in `.assetsignore`.
- After a URL change: update `projects.json` in the `hub` repo and the Obsidian note `Projects/PV Field Inspection.md`.
