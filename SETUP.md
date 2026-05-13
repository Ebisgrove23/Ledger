# Ledger PWA — Setup Guide

You have 5 files. Hosting them on GitHub Pages takes about 5 minutes and gives you a real installable app.

## Files in this bundle

- `index.html` — the app
- `manifest.webmanifest` — tells the browser this is an installable app
- `sw.js` — service worker (makes it work offline)
- `icon-192.png` — small icon
- `icon-512.png` — large icon
- `icon-maskable-512.png` — Android adaptive icon

All 6 files must live in the same folder on the server.

---

## Step-by-step: Host on GitHub Pages (free, ~5 min)

### 1. Make a GitHub account
If you don't have one, sign up at https://github.com (free).

### 2. Create a new repository
- Click the `+` in the top-right of GitHub → **New repository**
- Name it whatever you like (e.g. `ledger`)
- Set it to **Public** (required for free Pages hosting)
- Tick **Add a README file**
- Click **Create repository**

### 3. Upload the files
- On your new repo page, click **Add file** → **Upload files**
- Drag all 6 files from this bundle into the upload area
- Scroll down → click **Commit changes**

### 4. Turn on GitHub Pages
- In the repo, click **Settings** (top tab)
- In the left sidebar, click **Pages**
- Under **Source**, pick **Deploy from a branch**
- Under **Branch**, pick `main` and `/ (root)` → click **Save**
- Wait ~1 minute. The page will show a green box with your URL, something like:
  `https://yourusername.github.io/ledger/`

### 5. Install the app
- Open that URL in **Chrome** or **Edge** on your desktop
- Look at the right side of the address bar — you'll see a small **install icon** (a computer with a down arrow)
- Click it → **Install**
- The app opens in its own window and gets pinned to your taskbar/dock automatically

On **Mac**: it appears in your Applications folder and Dock.
On **Windows**: it appears in the Start menu and you can pin it to the taskbar.
On **mobile**: open the URL in Chrome/Safari → menu → "Add to Home Screen."

---

## Notes

- Your tasks are stored in your browser's localStorage on **each device separately** — they don't sync between devices.
- The app works fully offline once installed.
- To update the app later, just upload new versions of the files to the same repo. The service worker will pick up changes on next launch.
- If you ever want to take it offline, just delete the repo (or set it to Private).
