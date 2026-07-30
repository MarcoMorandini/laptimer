# Lap Timer — deploy to GitHub Pages

Files in this folder are the whole app. Nothing to build.

1. Create a new GitHub repo, e.g. `lap-timer`.
2. Upload the contents of this folder (index.html, manifest.webmanifest, sw.js, icon-*.png) to the repo root.
3. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main` / `/ (root)`. Save.
4. Wait ~1 minute, then open `https://<your-user>.github.io/lap-timer/` on your phone.
   GitHub Pages is served over HTTPS, which the camera requires.
5. iPhone: Share → "Add to Home Screen". Android Chrome: menu → "Install app".
   It then opens fullscreen, portrait, and works offline after the first load.

Notes
- Allow camera access on first "Enable camera" tap.
- The screen is kept awake during a race where the browser supports it (Android Chrome, iOS 16.4+).
- To ship an update: replace index.html and bump `CACHE = 'laptimer-v1'` in sw.js to v2, so phones fetch the new version.
