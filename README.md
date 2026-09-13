# sdmunoz.xyz

Personal link-in-bio page for **Samuel Muñoz** — Software developer & SRE engineer. A single static site with zero build step, zero trackers, and dark/light theme support.

## Features

- Fully static: plain HTML + CSS + a small vanilla JS snippet (theme persistence, share button, live link filter)
- Dark mode by default, with manual toggle (persisted in `localStorage`) and `prefers-color-scheme` support
- Grouped links: Support, Professional, Social, Content & Contact
- Responsive, accessible (semantic landmarks, focus states, `prefers-reduced-motion`)
- Self-hosted brand icons with official colors (no CDN dependency at runtime)

## Project structure

```
├── index.html          # Main page
├── privacy.html        # Privacy policy page
├── css/
│   ├── style.css       # Modern theme (the only stylesheet in use)
│   ├── normalize.css   # CSS reset
│   ├── brands.css      # Legacy LittleLink brand styles (unused, kept for reference)
│   └── skeleton-*.css  # Legacy LittleLink base styles (unused, kept for reference)
├── images/
│   ├── 35168329-9798-4f24-a9fa-aad87c7e16e0.jpg  # Profile photo
│   └── icons/          # Brand SVG icons (Simple Icons, brand colors)
└── fonts/              # Legacy bundled fonts (unused by the current theme)
```

## Getting started

No build tools required. Serve the folder with any static server:

```bash
npx serve .
```

then open the printed URL. Or simply open `index.html` in a browser.

## Customization

- **Links:** edit the `<nav class="links">` blocks in `index.html`. Each card is an `<a class="card">` with a `.tile` icon, `.card-text` (title + subtitle), and a `data-name` attribute used by the live filter.
- **Profile:** update the `.hero` section (photo in `images/`, name, bio, `.chips` list).
- **Theme:** colors and radii live in the `:root` / `[data-theme="light"]` blocks at the top of `css/style.css`.
- **Icons:** add 24x24 SVGs to `images/icons/`. Current icons come from [Simple Icons](https://simpleicons.org) with brand fills so they stay visible on the white tiles in both themes.

## Privacy

The site collects nothing: no backend, no analytics, no third-party requests. The only browser storage used is the theme preference in `localStorage`. See `privacy.html`.

## Credits

- Originally forked from [LittleLink](https://littlelink.io) (MIT). The current theme is a custom rewrite.
- Icons by [Simple Icons](https://simpleicons.org) (CC0).

## License

See [LICENSE.md](LICENSE.md).
