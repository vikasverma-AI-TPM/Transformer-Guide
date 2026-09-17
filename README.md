# Transformers, Interactively Explained

A single-file, self-contained interactive study guide for the Transformer architecture (attention, encoder/decoder, BERT vs GPT, and more). Everything — HTML, CSS, and JS — lives in `index.html`; there's no build step and no dependencies.

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. `transformer-guide`), don't initialize it with a README.
2. From this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Transformers interactive study guide"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. On GitHub: go to **Settings → Pages**, under "Build and deployment" set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, then **Save**.
4. Your site will be live in a minute or two at `https://<your-username>.github.io/<your-repo>/`.

## Deploy to Netlify

**Option A — drag and drop (fastest, no CLI needed):**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag this whole folder (or just `index.html`) onto the page.
3. Netlify assigns you a live URL immediately (e.g. `random-name-123.netlify.app`). You can rename the site later in **Site settings → Change site name**.

**Option B — connect the GitHub repo (auto-deploys on every push):**
1. Push this folder to GitHub first (see steps above).
2. In Netlify: **Add new site → Import an existing project → Deploy with GitHub**, pick the repo.
3. Build settings: leave **Build command** blank and set **Publish directory** to `.` (the repo root) — it's a static file, nothing to build.
4. Click **Deploy site**.

**Option C — Netlify CLI (if you have Node/npm installed locally):**
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod --dir=.
```

## Notes

- This is a static, self-contained page — no server, no build tooling, no external asset dependencies required at runtime.
- Any progress/mastery tracking in the guide is stored in the visitor's own browser (`localStorage`) and is per-device, not synced anywhere.
