# Wedding checklist PWA

Deploy: push this folder to the GitHub Pages repo. Open the URL on the phone, Share → Add to Home Screen.

Files: `index.html` (the whole app), `sw.js` (service worker), `manifest.webmanifest`, `icons/`.

Updates: `index.html` is fetched network-first, so a new push shows on the next open while online. `sw.js` is re-checked on every open and whenever the app returns to the foreground; a new worker takes over immediately and the page reloads once. The build stamp in `sw.js` changes on every build so the old cache is dropped.

Data lives in the phone's localStorage (offline-first). Use "Copy whole list" for a backup.
