# QR Forge

A free, client-side QR code generator — no signup, no server, nothing leaves your browser.

**Live demo:** _add your GitHub Pages / Firebase link here after deploying_

## Features
- **Text / URL** — basic QR generation
- **WiFi** — generates a scannable QR that auto-connects devices to a network
- **Contact card (vCard)** — scan to save a contact straight to your phone
- Custom foreground/background colors
- Adjustable size
- Optional logo overlay
- Download as PNG or SVG

## Run it locally
No build step, no npm install. Just open `index.html` in any browser.

```bash
# clone it
git clone https://github.com/YOUR_USERNAME/qr-forge.git
cd qr-forge

# open it — pick whichever works on your OS
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or, for live-reload while editing, serve it with any static server:
```bash
npx serve .
# or
python3 -m http.server 8080
```

## Deploy — GitHub Pages (free)
1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Source", select the branch (usually `main`) and root folder `/`.
4. Save. Your site will be live at `https://YOUR_USERNAME.github.io/qr-forge/` within a minute or two.

## Deploy — Firebase Hosting (free)
1. Install the Firebase CLI (one-time):
   ```bash
   npm install -g firebase-tools
   ```
2. Log in and initialize:
   ```bash
   firebase login
   firebase init hosting
   ```
   - When asked for your public directory, enter `.` (the repo root, since `index.html` is already here).
   - Choose "No" for single-page app rewrite (not needed here).
3. Deploy:
   ```bash
   firebase deploy
   ```
4. Firebase will print your live URL (something like `https://your-project.web.app`).

## Tech
Plain HTML/CSS/JS. Uses [qrcodejs](https://github.com/davidshimjs/qrcodejs) via CDN for QR encoding — no npm install, no build tooling, runs anywhere a browser can open a file.

## License
MIT — do whatever you want with it.
