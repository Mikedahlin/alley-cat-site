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
- `media/loops/hero-reel-1080.mp4` — hero background video (11.2s, black & white: Rich clip + shop wide shot, crossfaded through black; 1920×1080, muted/loop)
- `media/hero-poster.jpg` — first frame of the hero reel, shown before it loads
- `media/loops/piercing.mp4` + `media/loops/piercing-poster.jpg` — piercing section loop (black & white)
- `media/rich-loop.mp4` + `media/rich-poster.jpg` — Rich tattooing loop above the gallery
- `media/hero.mp4`, `media/loops/piercing-full.mp4`, `media/loops/cat-stabilized.mp4`, `media/loops/cat-clean-source.mp4`, `media/loops/cat-ai-source.mp4` — source cuts, not referenced by the page
- `media/frames/`, `media/sheets/` — extracted frames and contact sheets used to build the loops
- `media/work/` — tattoo gallery masters (~1400px, q85) — the WORK grid
- `media/flash/` — flash sheet catalog masters (~1400px, q85)
- `media/flash_sm/` — ~320px wheel thumbnails (what the flash wheel actually loads)
- `media/logo.jpg` — 1400×1400 square emblem (Open Graph / JSON-LD image, about section)
- `media/logo-mark.png` — 256×256 cat-head mark used in the header
- `media/favicon-32.png`, `media/icon-180.png`, `media/icon-512.png` — icons
- `media/favicon.svg` — legacy icon, no longer referenced
- `favicon.ico` — root fallback icon (16/32/48)
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
- **Replace the hero video:** drop a 1920×1080 H.264 MP4 in `media/loops/`, point the
  `.bgvid` `src` at it, and rebuild `media/hero-poster.jpg` from its first frame so the
  poster matches the video.
- **Change the favicon:** replace `media/favicon-32.png` (cat-head crop) plus `media/icon-180.png`
  and `media/icon-512.png` (full emblem), rebuild `favicon.ico` at 16/32/48, and bump the
  `?v=` query on the icon links in `index.html` so browsers drop the old cached icon.
  The header mark is `media/logo-mark.png` and the social/JSON-LD image is `media/logo.jpg`.

## Site map

`#home` hero → `#flash` flash wheel → `#work` gallery → `#coverup` cover-up slider → `#piercing` → `#book` contact
