# Chess 3D

3D chess in a single HTML file: arena maps, FPS mode, 30+ weapons with checkmate cutscenes, and online multiplayer via Firebase Realtime Database.

## Play locally
Open `index.html` in a browser (needs internet for the three.js and Firebase CDN scripts).

## Host on GitHub Pages
1. Create a new GitHub repo and upload everything in this folder (keep `index.html` at the root).
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
3. After a minute your game is live at `https://<your-username>.github.io/<repo-name>/`.

## Online multiplayer
Config lives in `FB_CFG` near the end of `index.html`. Publish `database.rules.json` in Firebase Console → Realtime Database → Rules. These rules are open (anyone can read/write `chess/*`), which is fine for playing with friends. The config has no API key: Realtime Database only needs the database URL, and access is controlled by the rules.

## Controls
- Orbit: drag to rotate, scroll or pinch to zoom, tap a piece then a square.
- FPS (button or `F`): WASD move, Shift sprint, Space jump, mouse look, click to shoot and move. `M` cycles maps.
