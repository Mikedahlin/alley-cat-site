# AGENTS.md — alley-cat-site

Rules for any AI agent working in this repo. These are not suggestions.

## Hard rule: no deploys without explicit approval

- **Never** run `git push`, create a Vercel deployment, or otherwise publish to `alleycatinkmn.com` unless the user explicitly approves **that specific change**.
- Editing files and committing locally are allowed. Publishing is a separate decision and belongs to the user.
- Approval is **per-change**. A "yes" to one change is not approval for the next one. Past approval is not standing consent.
- If it is unclear whether a change reaches the live site, treat it as live-affecting and ask first.

## Show before you ship

- Before committing site files, show `git diff` and a one-line statement of the live impact.
- For visual changes (logo, colors, photos, layout, fonts), show a preview or describe the exact change and **wait**. This agent cannot see images, so it must never ship a visual change the user has not confirmed.

## Ask first, always

- Deleting files, photos, or assets.
- Any Google Business Profile change (fields, photos, reviews, ownership).
- Force-push, history rewrite, branch deletion.
- Domain, DNS, or hosting configuration changes.

## Credentials

Never ask for, store, or type passwords, 2FA codes, or recovery codes. The user signs in themselves.

## Brand and facts

- Business name is always two words: **Alley Cat Ink**.
- Address: **113 Main St S, Hutchinson, MN 55350**.
- Never touch the Elkhorn, WI listing, MLR Assets, or 60BELOW.
- Do not invent hours, prices, services, or claims. If it is not confirmed, leave it blank or ask.

## Rollback

Keep the previous version of any asset being replaced, so every change can be undone in one commit.

## Deployment note

`vercel.json` uses `"outputDirectory": "."`, so **every file in this repo is publicly served**. Do not commit secrets, drafts, or private notes.
