# Precision Tinting Solutions — Demo Site

A single-page interactive demo site for a window tinting company, built to show
what's possible with a before/after slider, service area map, and a full tint
services breakdown.

## What's inside
- `index.html` — the entire site (HTML, CSS and JS in one file, no build step)

## What's real vs. placeholder
- **Real:** the business name and phone number (480-788-3159)
- **Placeholder / demo:** service area cities, warranty terms, pricing, "why us"
  claims, and all photography (AI-generated to demonstrate the before/after
  slider — swap these for real installation photos before going live)

## Deploying on Vercel via GitHub

1. Create a new GitHub repository and push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Initial demo site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new) and import the repository.
3. Framework preset: choose **Other** (it's a static HTML site, no build
   command or output directory needed — Vercel will serve `index.html`
   automatically).
4. Click **Deploy**. Vercel will give you a live `.vercel.app` URL in about a
   minute.

No environment variables, no `package.json`, and no build step are required.

## Swapping in real photos later
The before/after sliders and gallery images currently point to AI-generated
placeholder photos hosted on Higgsfield's CDN. To replace them:
1. Add your real photos to an `images/` folder in this repo.
2. In `index.html`, find each `<img src="https://...">` tag and change the
   `src` to the local path, e.g. `images/car-before.jpg`.
3. Commit and push — Vercel redeploys automatically.

## Customizing
- Colors, type and spacing are defined as CSS variables at the top of the
  `<style>` block in `index.html` — change `--copper`, `--glass`, `--ink`,
  etc. to adjust the palette.
- Each section is clearly commented/labeled by `<section id="...">` — services,
  service area, shade guide, and contact are all independent blocks you can
  reorder or edit directly.
