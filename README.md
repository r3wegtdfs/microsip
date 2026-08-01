# microsip.org — local mirror

An offline copy of `https://www.microsip.org/`, captured 2026-07-31.

Open `index.html` directly in a browser — all internal links and assets are
relative, so it works from `file://` with no server needed.

## Contents

- 87 HTML pages (the 15 main site pages, plus ~70 `/translation/translate/<id>` pages)
- 63 assets (CSS, JS, images, favicons) — ~9.3 MB total

## Changes made to the captured pages

This is not a byte-for-byte copy. Four deliberate changes:

1. **Links rewritten to relative paths** so the mirror works offline. Extensionless
   routes became directories (`/downloads` → `downloads/index.html`).
2. **Third-party tracking and ad code stripped**: Google Tag Manager, AdSense slots,
   Programmable Search, and the Google Translate widget. These can't work offline and
   would otherwise fire requests against the original site's analytics and ad accounts.
3. **jQuery vendored locally** (`js/jquery-1.11.3.min.js`, from the Google CDN, MIT
   licensed). The translation and custom-order pages depend on it.
4. **Not captured**: installer binaries (`/download/*.exe`) and the per-language
   export endpoints (`/translation/export/*`). Links to those still point at the live
   site so they keep working.

## Provenance

The site content, branding, screenshots, and logo belong to the MicroSIP project.
The MicroSIP *software* is GNU GPL v2, but that license covers the program, not the
website's text and images. This copy is fine as local reference or for studying the
markup; it should not be republished or served publicly, since a copy of a real
project's site presented as the real thing is indistinguishable from impersonation.
