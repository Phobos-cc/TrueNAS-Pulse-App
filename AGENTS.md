# TrueNAS Pulse App

Guidance for AI coding agents (Claude Code, Codex, Copilot, Cursor) when working in this repository.

## What this repo is

Public documentation site for **TrueNAS Pulse**, a closed-source native iPhone client for TrueNAS SCALE (App Store id `6759870893`, truenaspulse.com). This repo holds **no application source code** — the app itself lives elsewhere (see `docs/AGENTS.md`-style cross-reference in the sibling "TrueNAS Pulse Android" repo, which points to `/Users/chris/Developer/Xcode/TrueNAS Pulse` as the iOS product reference).

This repo is published as a static site via **GitHub Pages** at `legato3.github.io/TrueNAS-Pulse-App`, mirrored at `truenaspulse.com`.

## Relationship to other TrueNAS Pulse repos

- `TrueNAS-Pulse-App` (this repo) — public docs only, for the **closed-source iOS app**.
- `TrueNAS Pulse Android` — a separate, in-progress **Kotlin Multiplatform/Compose** port of the same product, with its own source tree and its own `CLAUDE.md`.
These are related by product/brand, not by shared code — do not assume shared build tooling or conflate the two when working across them.

## Stack

- Jekyll (`docs/_config.yml`), theme `jekyll-theme-cayman`, `kramdown` markdown renderer.
- No `Gemfile`, no `package.json`, no CI workflow in this repo — GitHub Pages builds the Jekyll site remotely on push. There is no local build/test/lint command to run.

## Layout

```
docs/
  _config.yml       — Jekyll site config (title, theme, markdown engine)
  _layouts/         — Jekyll page layout(s)
  _includes/        — Jekyll partials
  assets/           — images (app icon, screenshots)
  index.md          — site home
  changelog.md       — public changelog
  privacy.md         — privacy policy
  eula.md            — EULA
  terms.md           — terms of use
  faq.md              — FAQ
  contact.md          — contact page
LICENSE              — docs-only license ("all rights reserved", informational use)
```

Each `docs/*.md` page corresponds 1:1 to a page on truenaspulse.com (see the table in `README.md`).

## Conventions

- Keep edits scoped to `docs/*.md` content and `README.md`; there's no app code here to touch.
- This is public-facing legal/marketing copy (privacy policy, EULA, terms) — treat wording changes to those pages as significant, not cosmetic.
- No test suite, linter, or build step exists to verify changes locally; changes are only "live" once GitHub Pages rebuilds after push.
