# ResearchCamp — Thinka (Landing + Explorer)

A small static front-end project showcasing the "Thinka" coming-soon landing page and an interactive feature explorer (`thinka.htm`) with canvas visualizations.

## Live preview

- Open `index.html` in any modern browser (Chrome, Edge, Firefox). The landing page contains an animated background and an interactive visual card that links to `thinka.htm`.
- Open `thinka.htm` to view the multi-mode exploratory canvas and tabbed content panels.

## Key features

- Responsive landing page with animated background and a network-style canvas visualization (`#brainCanvas`).
- Document-pulse animation traveling between researcher and industry nodes.
- Clickable frame labels and pillar links that navigate to `thinka.htm` using URL hash anchors (e.g. `thinka.htm#researchers`).
- Hash-based tab switching in `thinka.htm` so deep links open the correct panel.
- Lightweight, dependency-free: vanilla HTML, CSS, and JavaScript.

## Files

- `index.html` — Coming-soon landing page, branding, email signup form, brain canvas visualization.
- `thinka.htm` — Feature explorer with multiple canvas modes, tabbed UI, and hash navigation.
- (Optional) any assets embedded as inline SVGs or data-URIs inside the HTML files.

## Development notes

- No build step required. Edit the HTML/CSS/JS files directly and refresh the browser to see changes.
- Canvas sizing uses parent bounding rect plus `window.devicePixelRatio` scaling. When editing layout, call `resize()` (window resize) or reload the page to ensure correct canvas scaling.
- Interactive elements (tabs, pillar links, frame labels) rely on `href` hash navigation and a `handleHash()`/`switchTo()` implementation in `thinka.htm`.
- CSS variables are defined in `index.html` under `:root` (colors, muted, faint, etc.) — reuse them for consistent theming.

## Troubleshooting

- If buttons appear unclickable, check for overlaying elements (canvas) and ensure interactive controls have `pointer-events: auto` and a higher `z-index` than the canvas.
- If canvas looks blurry, confirm `devicePixelRatio` scaling and that `cx.scale()` is not applied multiple times on repeated resizes.

## Contributing

- Edit files directly and open the pages locally to test. Keep changes focused and avoid introducing external dependencies.

## License

- No license file included. Add a `LICENSE` if you want to publish this project.

---

If you want, I can:

- Add a small local dev script (serve) and example `package.json`.
- Generate a short design/implementation doc for the canvas modes.
