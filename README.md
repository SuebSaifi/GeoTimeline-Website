# Timeline Visualizer — website

Static marketing and legal site for the Timeline Visualizer app. Plain HTML and one
stylesheet: no build step, no JavaScript, no external requests, no cookies or analytics.

```
website/
├── index.html         Home
├── features.html      Features
├── how-to-use.html    How to use the app
├── privacy.html       Privacy policy
├── terms.html         Terms and conditions
├── assets/css/style.css
└── assets/img/        mark.svg, app-icon.png, screenshots/
```

## Preview locally

```
cd website && python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy

Upload the folder to any static host (GitHub Pages, Netlify, Cloudflare Pages, S3).
`index.html` is the entry point; nothing needs to be compiled or configured.

## Keeping it accurate

- Content comes from `docs/privacy.md`, `docs/brand.md`, `docs/restore-google-maps-timeline.md`,
  `play-store/listing/en-US/`, and the app's own strings in `lib/l10n/app_en.arb`.
- The version badge on the home page and the effective dates on the legal pages are
  hard-coded — update them with each release.
- Screenshots are copied from `play-store/assets/screenshots/en-US/`; re-copy them when
  the store listing is refreshed.
- Palette follows `docs/brand.md` (`#E90064` brand, `#D0005A` interactive) and adapts to
  the visitor's light or dark system theme.
