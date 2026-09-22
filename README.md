# Wedding checklist PWA

Deploy: push this folder to a GitHub Pages repo (or any HTTPS host). Open the URL on the phone, Share → Add to Home Screen.

Files: `index.html` (the whole app), `sw.js` (service worker), `manifest.webmanifest`, `icons/`.

Updates: every time you push a new `index.html` and `sw.js`, the app fetches `index.html` network-first, so the new version shows on the next open while online. `sw.js` is re-checked on every open and whenever the app comes back to the foreground; when a new worker installs it takes over immediately and the page reloads once. Bump the `build` stamp in `sw.js` (or just re-run the build) so the old cache is dropped.

Data lives in the phone's localStorage only (offline-first). Use "Copy whole list" for a backup.
