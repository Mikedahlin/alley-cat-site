# ALLEY CAT INK — Static Site

Single-page static site for Alley Cat Ink (Hutchinson, MN). No build step, no dependencies, no framework.

## Canonical source

This folder is the source of truth:

`C:\Users\harle\Projects\WEB-PROJECTS\alley-cat-site-main\alley-cat-site`

Do not deploy from the parent `alley-cat-site-main` folder or any older copy. This folder is the Git repository and the Vercel root.

## Deploy (Vercel)

- Import repo, framework preset: **Other**, output dir: repo root.
- Or run `npx vercel` from this folder.

## Business NAP (keep in sync with Google Business Profile)

- Name: **Alley Cat Ink**
- Address: **113 Main St S, Hutchinson, MN 55350**
- Phone: **(320) 699-1012**
- Hours: **Tue–Sat 12:00 PM – 7:30 PM**
- Website: **https://alleycatinkmn.com**

If any of these change, update the visible page, the JSON-LD block in `index.html`, the Google Business Profile, and the Facebook page in the same pass.

## Structure

- `index.html` — all markup, styles, and JS (one file, intentionally)
- `media/hero.mp4` — hero background video (muted/loop/playsinline, mobile-safe)
- `media/work/` — tattoo gallery masters (~1400px, q85) — the WORK grid
- `media/flash/` — flash sheet catalog masters (~1400px, q85)
- `media/flash_sm/` — ~320px wheel thumbnails (what the flash wheel actually loads)
- `media/favicon.svg`, `media/favicon-32.png`, `media/icon-180.png`, `media/icon-512.png` — icons
- `favicon.ico` — root fallback icon (some browsers and previews request `/favicon.ico`)
- `robots.txt` — crawler rules + sitemap reference
- `sitemap.xml` — single-page sitemap
- `GBP-PLAYBOOK.md` — Google Business Profile field values, photo plan, and review process
- `gbp-baseline.csv` — before/after tracking template for the GBP

## Editing

- **Add a flash design:** drop the full image in `media/flash/`, a ~320px-wide copy
  in `media/flash_sm/`, and add one entry to the `PIECES` array in `index.html`.
- **Add a work photo:** drop an optimized (~1400px q85) image in `media/work/` as `wNN.jpg`
  and add one `<figure class="witem">` line in the grid.
- **Remove either:** delete its figure line / `PIECES` entry, then the files.
- **Change the favicon:** replace the files in `media/`, rebuild `favicon.ico`, and bump the
  `?v=` query on the icon links in `index.html` so browsers drop the old cached icon.

## Site map

`#home` hero → `#flash` flash wheel → `#work` gallery → `#coverup` cover-up slider → `#piercing` → `#book` contact
