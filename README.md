## CleanX

Personal userscript (and Chrome extension) for X/Twitter that filters posts by country, region, or language with optional highlighting.

### Features
- Add or remove blocked countries, regions, and language scripts (no defaults).
- Choose filter behavior: hide or highlight matches (red border/background). Region-only accounts can be highlighted in yellow.
- Per-session and lifetime counts persisted to IndexedDB; exports available from the UI.
- Fetches profile “About” data to detect country/region and username change counts.
- Settings button in the left nav (🚫 icon) opens the modal for edits.

### Usage
1) Userscript: install `CleanX-user.js` in your userscript manager.  
2) Chrome extension: load `extension/` as an unpacked extension in `chrome://extensions` (Developer Mode).  
3) Open X/Twitter and click the 🚫 CleanX button under Profile in the left nav.  
4) Add countries/regions/languages; toggle block vs highlight and region-only highlight.  
5) Reload to apply; use Export DB for debugging or backup.

### Development Notes
- No build step; edit `CleanX-user.js` directly.
- Optional format: `npx prettier --check "CleanX-user.js"`.
- Primary storage: `localStorage` + IndexedDB (`known` store for users, `stats` for totals).
- Extension entrypoint: `extension/content.js`, manifest at `extension/manifest.json`.
