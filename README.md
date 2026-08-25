# Erik Woods — Engineering Portfolio

A static, recruiter-facing portfolio for Erik Woods, a Computer Engineering student at the University of Florida. The site is built with semantic HTML, CSS, and lightweight JavaScript and is intended to publish directly through GitHub Pages.

## Structure

```text
/
├── index.html              # Content and semantic page structure
├── css/styles.css          # Design system and responsive layouts
├── js/main.js              # Navigation, reveals, and project filters
└── assets/
    ├── favicon.svg
    └── images/
        └── weather-dashboard.png
```

There is no build step and no backend. For local development, run a static server from the repository root:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Updating projects

Flagship projects are written directly in `index.html` because their layouts are intentionally different. To update one, edit its description, decision notes, stack line, repository URL, and visual together.

Archive projects use repeated `.archive-row` articles. To add one:

1. Copy an existing `.archive-row`.
2. Set `data-category` to `hardware`, `systems`, `data`, or multiple space-separated categories.
3. Update the area, title, specific one-line description, stack, accessible link label, and verified repository URL.
4. Use `In development` only when the public repository supports that status.

The filter behavior in `js/main.js` reads `data-category` automatically; no project totals or filter counts need updating.

## GitHub Pages

The repository is intentionally compatible with GitHub Pages publishing from the root of the `main` branch. All asset URLs are relative, so the site also works from a local static server without configuration.
