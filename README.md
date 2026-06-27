# NYC Live 2026 — Crew Launchpad

A one-tap launchpad that links the broadcast crew to the NYC Live 2026 production files in Google Drive.

**Live site:** https://alanbrown8068.github.io/nyc-live-2026/

Add it to a phone home screen: open the link in Safari (iPhone) or Chrome (Android) → **Share / menu → Add to Home Screen**. You'll get the NYC Live icon.

---

## What's in this repo

| File | Purpose |
|------|---------|
| `index.html` | The launchpad page (all links + styling, self-contained) |
| `manifest.webmanifest` | Home-screen app config (name, colors, icons) |
| `icon-180.png` / `icon-192.png` / `icon-512.png` | Home-screen icons |
| `logo.png` | *(optional)* the real NYC Live logo for the header |

---

## Add the real logo

The header shows a built-in mountain-and-flag mark until the real logo is added.

1. Download **`NYC Live logo v03.png`** from the Drive *Logo* folder.
2. Rename it **`logo.png`**.
3. In this repo: **Add file → Upload files**, drag it in, **Commit changes**.

The header swaps to the real logo automatically — no code change needed.

---

## Update the links

Two ways:

1. **Drop files into the Drive folder.** Add or rename files/folders inside the `NYC Live 2026` Drive folder. The scheduled refresh (below) picks them up and updates this page.
2. **Edit `index.html` directly.** Each tile is an `<a class="card" href="…">` block, grouped into the *Workbooks*, *Docs*, and *Content & Assets* sections. Edit and commit.

---

## Auto-refresh

A scheduled Cowork task re-reads the `NYC Live 2026` Drive folder once a day during the trip and regenerates this page.

- When your Chrome is connected, it commits the update here and the site redeploys automatically (~1 min).
- When it can't reach your browser, it prepares the updated `index.html` and messages you with what changed, so you can upload it manually.

---

## How it's hosted

GitHub Pages, `main` branch, root folder (`Settings → Pages`). HTTPS enforced.
The repo is **public** (free Pages requirement), so file *names* are visible to anyone with the link — but the Drive files themselves keep their own Google permissions.
