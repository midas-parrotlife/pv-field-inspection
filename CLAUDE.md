# CLAUDE.md — pv-field-inspection

- Single-file app: everything lives in `index.html`. Keep it dependency-free and working offline on a phone.
- Deploy is automatic on push to `main` (Cloudflare Workers Builds). Never deploy by hand.
- Anything added to the repo root is served publicly unless listed in `.assetsignore`.
- `index.html` has a Content Security Policy that pins each inline `<script>` by SHA-256 hash and sets `connect-src 'none'`. After changing any script, recompute the hashes, or the app stops running.
- Script tags carry `data-cfasync="false"` and the body is wrapped in `<!--email_off-->`, so Cloudflare Rocket Loader and e-mail obfuscation leave the scripts unchanged. Do not enable other Cloudflare features that rewrite HTML or inline scripts.
- Treat imported ZIP data as untrusted: validate in `sanitizeRecord()` and never put record fields into `innerHTML` unescaped.
- After any deploy or URL change: update `projects.json` in the `hub` repo and the Obsidian note `Projects/pv-field-inspection.md`.
- Commit with the GitHub noreply address, never a parrotlife.nl alias.
