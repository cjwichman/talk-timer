# Talk Timer

Full-screen countdown timer for conference presentations. Runs in any modern browser and installs as a home-screen app on iPad or iPhone.

- Large white digits on black.
- Background turns yellow at 3:00 remaining and red at 1:00 remaining (both adjustable).
- At 0:00 the display flashes red/black for 5 seconds, then holds solid red at 0:00.
- A smaller "Extra time" counter appears under 0:00 and counts the time elapsed since the talk ended (for Q&A or overrun). Pause and restart apply to it as well.
- Presets of 7, 10, 12, 15, and 20 minutes, plus a custom minute setting with −/+ buttons (hold to repeat). An optional seconds setting (15-second steps, or type any value) sits behind **+ Add seconds**.
- Screen stays awake while the timer screen is open (Screen Wake Lock API, iOS/iPadOS 16.4+ and current desktop browsers).
- Works offline after the first load. Settings persist between sessions.

## Use

1. Pick a length, adjust warnings if needed, and press **Ready**.
2. Tap the timer (or press Space) to start. Tap again to pause.
3. Controls appear after a tap: Start/Pause, Restart, Setup, Fullscreen.

| Key | Action |
|---|---|
| Space | Start / pause |
| R | Restart at full length |
| F | Toggle fullscreen |
| Esc | Back to setup (when not fullscreen) |
| Enter | Start from setup screen |

## Hosting on GitHub Pages

1. Push this folder to a GitHub repository.
2. Repository **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
3. The site appears at `https://<user>.github.io/<repo>/` after a minute or two.

## iPad / iPhone install

Open the Pages URL in Safari, then **Share → Add to Home Screen**. The home-screen version opens without browser chrome. iPhone Safari has no fullscreen mode for web pages, so the Fullscreen button is hidden there and the home-screen version is the way to get a full-screen display. Rotate the phone to landscape for the largest digits.

## Files

| File | Purpose |
|---|---|
| `index.html` | App (markup, styles, and script in one file) |
| `manifest.webmanifest` | Home-screen app metadata |
| `sw.js` | Service worker for offline use |
| `icons/` | App icons |

Updating `sw.js` (for example, bumping `CACHE` to `talk-timer-v2`) forces installed copies to refresh cached files.
