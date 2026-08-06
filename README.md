# Daily Tracker — repaired

A dependency-free daily task and study tracker. It runs entirely in the browser and stores data in `localStorage`; no backend or account is required.

## What was broken in the original repository

The original `dailytracker.html` ended in the middle of this JavaScript statement:

```js
const h = Math.
```

That made the whole script invalid, so the browser stopped before rendering the app. The repository also did not contain an `index.html`, which is the standard GitHub Pages entry file.

## What this repaired version includes

- Complete task add / complete / delete behavior
- Persistent study timer and daily totals
- Adjustable daily study goal
- Study history grouped by local calendar day
- Safe text rendering for user-entered tasks
- Mobile and keyboard-accessible UI
- `index.html` for GitHub Pages
- A GitHub Actions Pages deployment workflow
- The old `dailytracker.html` path retained for compatibility

## Run locally

Open `index.html` directly in a modern browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy with GitHub Pages

1. Push these files to the `main` branch of a GitHub repository.
2. In **Settings → Pages**, set **Source** to **GitHub Actions**.
3. Open the **Actions** tab and wait for **Deploy static site to GitHub Pages** to complete.
4. The workflow summary will show the deployed URL. For a project repository it normally follows:

   `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`

## Data note

Tracker data stays in the browser and does not sync between browsers or devices. Clearing site data also clears the tracker data.
