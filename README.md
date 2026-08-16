# testGithubPage

Static GitHub Pages site that shows an OpenStreetMap map with Leaflet and (when allowed) the visitor's current location.

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
- On page load, the browser requests geolocation permission.
- If access is granted, the map centers on the user and places a marker.
- If access is denied or fails, a clear message is shown and the map remains usable.
- Geolocation generally works best over HTTPS (GitHub Pages) or localhost.
