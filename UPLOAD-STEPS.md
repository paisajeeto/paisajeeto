# PaisaJeeto — GitHub Pages upload steps

The PaisaJeeto app is already built to read its live configuration from:

    https://paisajeeto.github.io/paisajeeto/config.json

Follow these steps once, and from then on you can change games, rewards and
settings from the admin page — no app update needed.

## Step 1 — Create the repository

1. Go to https://github.com/new (signed in as **paisajeeto**).
2. Repository name: type exactly **paisajeeto** (all lowercase).
3. Choose **Public** (GitHub Pages on a free account needs a public repo).
4. Do NOT tick "Add a README file" — the repo must start empty so the upload
   is clean.
5. Click **Create repository**.

## Step 2 — Upload the files

1. On the new repo page, click **uploading an existing file**
   (or: Add file → Upload files).
2. Open this `github-pages` folder on your computer and select **ALL of its
   contents** — the files and the `games` folder itself:
   - `config.json`
   - `admin.html`
   - `index.html`
   - `privacy.html`
   - `UPLOAD-STEPS.md`
   - the `games` folder (with all 15 game files inside)
3. Drag them into the GitHub upload box. **Upload the contents of the folder,
   not the folder itself** — `config.json` must end up at the top level of the
   repo, next to `admin.html`.
4. Click **Commit changes**.

## Step 3 — Turn on GitHub Pages

1. In the repo, open **Settings** (top tab bar).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment" → Source: **Deploy from a branch**.
4. Branch: choose **main**, folder: **/ (root)**.
5. Click **Save**.

## Step 4 — Confirm it works

1. Wait about **1 minute** for the first deployment.
2. Open this address in your browser:

       https://paisajeeto.github.io/paisajeeto/config.json

   You should see the app configuration text (starting with
   `{"appName":"PaisaJeeto", ...}`). If you see a 404, wait another minute and
   refresh; also double-check the repo is named exactly `paisajeeto` and that
   `config.json` is at the top level, not inside a subfolder.
3. Also check the admin page loads:
   https://paisajeeto.github.io/paisajeeto/admin.html

## Good to know

- The app already points at this URL (it was baked in during the PaisaJeeto
  rebuild). Until the repo exists, the app simply uses its built-in copy of
  the configuration, so nothing breaks.
- To change games/rewards later: open the hosted **admin.html**, load the
  config, edit, and save it back to GitHub (or upload a new `config.json`).
  The app picks changes up on its next launch — no rebuild, no Play update.
- New game = one HTML file in `games/` + one card in the config.
