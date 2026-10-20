# TUSKOLIFT — Static Website

Static export of the TUSKOLIFT industrial lifting-equipment website, hosted with
**GitHub Pages**.

- **Live URL:** https://siriusl1.github.io/
- **Source:** exported from the local WordPress + Vue build (`http://tuskolift/`)
- **Host:** GitHub Pages (user site, served from the repository root)

## What this is

A static mirror of the site's public pages: home, about, offerings, products,
blog and posts, contact, legal pages, plus all theme CSS/JS and media assets.

## Important limitations of a static export

This is a **snapshot**, not the live CMS. Some dynamic features therefore do not work:

| Feature | Status on GitHub Pages |
|---|---|
| Page navigation, images, styling | ✅ Works |
| Blog posts, legal pages | ✅ Works |
| Product catalog (`/products/`) | ⚠️ Server-rendered links work; the Vue interactive filter/listing needs the WordPress REST API and will not populate — the `<noscript>` fallback list is what renders |
| Inquiry / contact forms | ❌ POSTs to WordPress; cannot submit on a static host |
| “Suggest a topic” form | ❌ Same reason |
| Search, comments, RSS | ❌ Not available |

To submit an inquiry, use the form on the **live WordPress site** (or the contact
details once the production domain is configured).

## Re-generating this export

The static files were produced by crawling the local site at `http://tuskolift/`
(Local by Flywheel) and rewriting internal origin URLs to root-absolute paths,
since GitHub Pages serves this repo at the domain root.

## Notes

- `.nojekyll` is present so GitHub Pages serves files verbatim.
- `404.html` is a copy of the home page (GitHub Pages fallback).
