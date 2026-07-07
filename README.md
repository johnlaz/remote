# Media Remote — Landing Page

Single-file landing page for Media Remote, matching the Lazzaro Standard
design language (dark, gold/teal, Playfair Display + DM Sans) used across
the rest of the portfolio.

## Deploy

```
johnlaz.github.io/mediaremote/
├── index.html              ← this landing page
└── assets/
    └── mediaremote.zip     ← the downloadable app package
```

Push both to the `mediaremote` folder in your GitHub Pages repo. No build
step — `index.html` is plain HTML/CSS, no dependencies beyond two Google
Fonts loaded via `<link>`.

## Updating the download link

Every download button points to the relative path `assets/mediaremote.zip`.
To ship a new version:

1. Replace `assets/mediaremote.zip` with the new build
2. Update the version badge in the hero (`v5.3 · Windows · runs locally`)
   and the phone mockup's status line (`v5.3`) to match
3. Nothing else needs to change — same filename, same links

## Structure

| Section | What it is |
|---|---|
| Header | Sticky nav, brand mark, Download button |
| Hero | Headline + CTA on the left, phone mockup on the right |
| Features | 4 cards — Kodi, Screen Mirror, customization, Copilot/Voice Access |
| Setup | 3 numbered steps: download, run Setup.bat, open on phone |
| Final CTA | Repeats the download button before the footer |

The phone mockup in the hero is hand-built CSS recreating the actual
launcher grid (real tile colors, real bottom nav) — not a stock device
illustration. If the real app's tile colors or nav icons change, update
`.ph-tile` and `.ph-nav-item` in the `<style>` block to match, so the
mockup stays honest to the current build.

## Editing copy

All text lives directly in the HTML — no CMS, no template engine. Search
for the section by its heading text and edit in place.

## Browser support

Modern evergreen browsers (Chrome, Edge, Safari, Firefox). Uses CSS Grid,
`backdrop-filter`, and `aspect-ratio` — no polyfills included, matches the
same baseline as the Media Remote app itself.

---
Media Remote — © 2026 LAZLAB Creations
