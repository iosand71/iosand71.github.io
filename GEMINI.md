# Project Overview

This is a personal website and blog for Andrea Iosio, hosted on GitHub Pages at www.iosand.com. Originally built with Hugo (version 0.74.3), now maintained as static HTML.

## Project Structure

```
iosand71.github.io/
├── index.html            # Home page
├── pages.json            # Content manifest (read this first!)
├── _template.html        # Template for new pages
├── css/
│   ├── styles.css        # Editable CSS source
│   └── concated.min.css  # Minified CSS (avoid editing)
├── js/
│   └── core.min.js       # JavaScript (hamburger menu)
├── img/                  # Images and assets
├── font/                 # Lato font files
├── posts/                # Blog posts
├── categories/           # Category pages
├── tags/                 # Tag pages
├── covid19-*.html        # COVID-19 data pages
├── CNAME                 # GitHub Pages domain config
└── sitemap.xml           # XML sitemap
```

## Before Making Changes

1. **Read `pages.json`** - understand site structure and all pages
2. **Use `_template.html`** - copy this when creating new pages
3. **Edit `css/styles.css`** - formatted CSS for style changes

## Running Locally

```bash
python -m http.server 8000
```

Then open http://localhost:8000

## Common Tasks

### Add a menu item
Edit `index.html`, find `<ul id="menu" class="hamburger-menu-overlay">` and add:
```html
<li><a href="/page-url.html" class="hamburger-menu-overlay-link">Page Title</a></li>
```

### Add a new page
1. Create a new `.html` file in root
2. Copy structure from existing page
3. Add link in hamburger menu

### Update site metadata
Edit `index.html`:
- `<title>` - page title
- `<meta name="description">` - site description
- `<h1 class="nav-header">` - header text

## Deployment

Push to `master` branch - GitHub Pages auto-deploys.

## Important Files

| File | Purpose |
|------|---------|
| `CNAME` | Custom domain (www.iosand.com) - do not delete |
| `css/concated.min.css` | Main styles - avoid direct edits |
| `sitemap.xml` | Update when adding new pages |
