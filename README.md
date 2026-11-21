# Flag Locker

An installable (PWA) inventory app for national flags and International Code of Signals flags.
Track good / bad / total counts, par levels, size, material, location, notes and a photo for each flag,
and export everything to CSV for Excel. Works offline once installed. Data is stored on the device (localStorage).

## Files
- `index.html` – the whole app (HTML, CSS, JS)
- `manifest.webmanifest` – PWA install info
- `sw.js` – service worker (offline cache)
- `icons/` – app icons (180, 192, 512, maskable 512)
- `.nojekyll` – tells GitHub Pages to serve files as-is

## Publish on GitHub Pages
1. Create a new GitHub repository (e.g. `flag-locker`) and upload all of these files to the repo root.
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
3. After a minute your app is live at `https://<your-username>.github.io/flag-locker/` (HTTPS is required for install and offline).

## Install on your phone
- **iPhone (Safari):** open the URL → Share → *Add to Home Screen*.
- **Android (Chrome):** open the URL → ⋮ menu → *Install app* / *Add to Home screen*.

## Updating
Edit the files, then change `CACHE = 'flag-locker-v1'` in `sw.js` to `v2`, `v3`, … so installed copies pick up the update.

## Notes
- Data lives in each browser/device separately. On iPhone, the home-screen app has its own storage, separate from Safari, so enter data after installing.
- Signal flag artwork is simplified; numeral pennants are shown as labelled icons. Check against the official ICS publication.
