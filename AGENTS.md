# Repository Guidelines

## Project Structure & Module Organization

This repository contains the static Iosand.com site hosted through GitHub Pages. `index.html` is the homepage. `archived/2026/covid19-*.html` contains archived, unmaintained notebook-exported data reports; the year directory records the year of archiving. These reports are not linked from the homepage. The original homepage is preserved at `archived/2026/homepage-original.html`.

`css/home.css` styles the homepage, while `archived/2026/homepage-original.css` supports the preserved original homepage. Images live in `img/`; the archived homepage uses `font/LatoLatin-Bold.woff2`. `pages.json` inventories content and assets; `sitemap.xml` and `index.xml` provide the sitemap and RSS feed. `CNAME` configures the custom domain.

## Build, Test, and Development Commands

There is no package manifest, build pipeline, or dependency installation step. Serve the repository directly:

- `python3 -m http.server 8000` — preview at `http://localhost:8000`; serving from the repository root preserves root-relative asset links.
- `python3 -m json.tool pages.json > /dev/null` — check manifest JSON syntax.
- `git diff --check` — catch whitespace errors before committing.

## Coding Style & Naming Conventions

Use two-space indentation in hand-maintained HTML, CSS, and JSON, following nearby code. Prefer lowercase, hyphen-separated page names and CSS classes, such as `my-new-page.html` and `site-header`. No formatter or linter is configured.

Keep Italian-facing content consistent with existing pages. Preserve semantic markup, image alternative text, keyboard focus styles, and responsive layouts. Edit `css/home.css` for homepage changes and avoid unrelated formatting of notebook exports.

Treat files under `archived/` as historical snapshots. Do not modernize their dependencies, styling, or content unless explicitly requested. Record archived pages in `pages.json` with `status: "archived"`, `maintained: false`, and `archivedYear`.

## Testing Guidelines

There is no automated test framework or coverage threshold. Preview changed pages at desktop and mobile widths. Check links, asset loading, keyboard navigation, browser console errors, and affected report charts or menus.

## Commit & Pull Request Guidelines

History uses short, action-oriented subjects, sometimes prefixed with `feat:` or `refactor:`. Follow that pattern and keep commits focused. Pull requests should describe the change, affected pages, and validation performed; link relevant issues and include screenshots for visual changes.

## Content Updates

Update `pages.json` and applicable sitemap or feed entries when adding, removing, or renaming pages. Keep archived pages marked with their archive year and maintenance status.
