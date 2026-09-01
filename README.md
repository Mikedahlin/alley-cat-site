# ALLEY CAT INK — Static Site

Single-page static site for Alley Cat Ink (Hutchinson, MN). No build step, no dependencies, no framework.

## Deploy (Vercel)
- Import repo, framework preset: **Other**, output dir: repo root.
- Or run `npx vercel` from this folder.

## Structure
- `index.html` — all markup, styles, and JS (one file, intentionally)
- `media/hero.mp4` — hero background video (muted/loop/playsinline, mobile-safe)
- `media/work/` — tattoo gallery masters (~1400px, q85) — the WORK grid
- `media/flash/` — flash sheet catalog masters (~1400px, q85)
- `media/flash_sm/` — ~320px wheel thumbnails (what the flash wheel actually loads)

## Editing
- **Add a flash design:** drop the full image in `media/flash/`, a ~320px-wide copy
  in `media/flash_sm/`, and add one entry to the `PIECES` array in `index.html`.
- **Add a work photo:** drop an optimized (~1400px q85) image in `media/work/` as `wNN.jpg`
  and add one `<figure class="witem">` line in the grid.
- **Remove either:** delete its figure line / `PIECES` entry, then the files.

## Site map
`#home` hero → `#flash` flash wheel → `#work` gallery → `#coverup` cover-up slider → `#piercing` → `#book` contact
