# Claude Code Instructions

This is Andrea Iosio's personal website hosted on GitHub Pages at www.iosand.com.

## Site Structure

- **Static HTML site** - Originally generated with Hugo, now maintained as static HTML
- **Deployment**: Push to `master` branch auto-deploys via GitHub Pages

## Key Files

| File | Purpose |
|------|---------|
| `index.html` | Home page |
| `pages.json` | **Content manifest** - lists all pages and assets |
| `_template.html` | **Template for new pages** - copy this to create pages |
| `css/styles.css` | **Editable CSS source** - formatted and documented |
| `css/concated.min.css` | Main stylesheet (minified, avoid editing) |
| `js/core.min.js` | JavaScript (hamburger menu) |
| `img/` | Images and assets |
| `font/` | Lato font files |
| `posts/` | Blog posts |
| `covid19-*.html` | COVID-19 data pages (Jupyter notebooks) |

## Before Making Changes

1. **Read `pages.json`** to understand site structure
2. **Use `_template.html`** when creating new pages
3. **Edit `css/styles.css`** for style changes (not the minified version)

## Common Tasks

### Add a menu item
Edit `index.html`, find the `<ul id="menu" class="hamburger-menu-overlay">` section and add:
```html
<li><a href="/page-url.html" class="hamburger-menu-overlay-link">Page Title</a></li>
```

### Update meta description
Edit `index.html`, find and modify the `<meta name="description" content="...">` tag.

### Change site title
Edit `index.html`, modify the `<title>` tag and `<h1 class="nav-header">` content.

### Add a new static page
1. Create a new `.html` file in the root directory
2. Copy structure from an existing page
3. Add navigation link in `index.html` hamburger menu

## CSS Classes Reference

| Class | Purpose |
|-------|---------|
| `.nav-bar` | Top navigation bar |
| `.hamburger-menu` | Mobile menu container |
| `.hamburger-menu-overlay` | Mobile menu overlay |
| `.card-container` | Main content area |
| `.list-header` | Page header section |
| `.motto` | Motto image styling |
| `.content` | White content card |
| `.post` | Blog post styling |

## Important Notes

- **Do not modify** `css/concated.min.css` directly unless necessary - it's minified
- **Images** go in `img/` directory
- **Test locally** with `python -m http.server 8000` before pushing
- **CNAME** file contains the custom domain - do not delete

## Git Workflow

1. Make changes
2. Test locally at http://localhost:8000
3. Commit with descriptive message
4. Push to master (auto-deploys)
