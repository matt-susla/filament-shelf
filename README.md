# Filament Shelf

A phone-first tracker for 3D printing filament. Keep a shelf of spools with grams left, log prints to count filament down automatically, see cost per print, and get low-stock warnings.

It is a plain web app: no build step, no server, no account. Data is saved on the device that uses it.

## What's in this folder

| File | What it does |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | Name, icon and full-screen settings for "Add to Home Screen" |
| `sw.js` | Offline support (caches the app after the first visit) |
| `icons/` | Home-screen icon, favicon and the logo in the header |

## Put it on GitHub Pages (about 5 minutes, all in the browser)

1. Sign in at [github.com](https://github.com). Create a free account if you don't have one.
2. Click **+** (top right) → **New repository**.
   - Repository name: `filament-shelf`
   - Choose **Public** (free GitHub Pages needs a public repository)
   - Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Drag **everything inside this folder** onto the page: `index.html`, `manifest.webmanifest`, `sw.js`, `README.md` and the `icons` folder. Drag the files themselves, not the folder that holds them, so `index.html` sits at the top level.
5. Click **Commit changes**.
6. Go to **Settings** → **Pages** (left sidebar).
   - Under **Build and deployment**, set **Source** to **Deploy from a branch**.
   - Set **Branch** to `main` and the folder to `/ (root)`, then click **Save**.
7. Wait a minute or two and refresh the Pages screen. It shows your site address, for example
   `https://YOUR-USERNAME.github.io/filament-shelf/`

## Add it to your iPhone

1. Open the site address in **Safari** (not Chrome; only Safari can add a full-screen app).
2. Tap the **Share** button → **Add to Home Screen** → **Add**.
3. Open it from the home screen. It runs full screen with the spool icon, and works offline after the first open.

## Your data

- Spools and prints are saved **on the phone**, inside the home-screen app. Nothing is sent anywhere, so people who visit the same address can't see your data.
- The home-screen app keeps its own data, separate from Safari. Use the app from the home-screen icon.
- Deleting the home-screen app deletes its data. Use **Stats → Backup → Export backup** now and then and save the file to Files or iCloud Drive. **Restore from backup** brings it back on a new phone.

## Updating the app later

1. In the repository, click **Add file** → **Upload files** and drop in the changed files (same names replace the old ones). Commit.
2. In `sw.js`, change `VERSION` (for example `filament-shelf-v1` → `filament-shelf-v2`) so phones download the new copy instead of using the cached one.
3. On the phone, close and reopen the app. It may take one extra reopen to show the new version.
