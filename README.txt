# Year Tracker — Offline PWA

This folder is a ready-to-host Progressive Web App.

## What's included
- `index.html` — your tracker, adapted for offline use
- `manifest.webmanifest` — installable app metadata
- `sw.js` — service worker that caches the app shell
- `icons/` — Android/PWA icons

## Host it for free with GitHub Pages
1. Sign in to GitHub and create a new repository (for example, `year-tracker`).
2. Upload **all files and folders** from this package. Keep the folder structure unchanged.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site. It will show you an HTTPS address.
7. Open that HTTPS address in Chrome on your Android phone.
8. Open Chrome's menu and choose **Install app** (or **Add to Home screen**).

## Offline test
Open the installed app once while online and wait for it to load. Then turn on airplane mode and reopen it. The app shell should load offline.

## Important data note
Your tracker data is saved in this browser installation using `localStorage`. It is not uploaded or synchronized to an account. Keep the same installed app/site address and do not clear Chrome's site data, or the saved tracker data may be lost. Consider periodically keeping a separate backup if the data is important.

## Notes
- The Google Fonts network dependency was removed, so the app uses its built-in system font stack offline.
- The optional Claude account-sync integration was removed from this standalone build. The tracker continues to save locally.
- This package must be hosted over HTTPS (GitHub Pages provides HTTPS) for service-worker installation. Opening `index.html` directly from the phone's file manager will not enable full PWA installation/offline caching.


## Backing up and restoring your tracker
- In the app, open the **Backup & restore** card and tap **Export backup**.
- Your phone downloads a JSON backup file. Keep it somewhere safe (for example, Google Drive or another storage location).
- To restore, open the app, tap **Import backup**, select the JSON backup file, and confirm.
- Importing replaces the current tracker data with the selected backup. Export your current data first if you may need it.
- A backup is a copy; exporting does not automatically upload or sync it.
