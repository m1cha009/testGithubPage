# 1

Static GitHub Pages site that shows an OpenStreetMap map with Leaflet and can record, save, and reload movement trails in the browser.

## Run locally

This is a no-build static site. Open `index.html` directly, or serve the repo with any static server.

## Deploy on GitHub Pages

1. Push this repository to GitHub.
2. In GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` (or your default branch)
   - **Folder**: `/ (root)`
4. Save and wait for Pages to publish.

Your site will be available at:

`https://<your-username>.github.io/testGithubPage/`

## Behavior

- The map loads immediately using OpenStreetMap tiles.
- Click **Start tracking** to request geolocation permission and begin recording points.
- While tracking is active, the page updates the current marker and draws the live trail on the map.
- Click **Stop tracking** to stop geolocation watching.
- After stopping, click **Save current trail** to store the recorded points in browser `localStorage`.
- Saved trails can be **loaded** or **deleted** later from the same browser/device.
- If access is denied or fails, a clear message is shown and the map remains usable.
- Geolocation generally works best over HTTPS (GitHub Pages) or localhost.
