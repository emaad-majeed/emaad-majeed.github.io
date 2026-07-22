# emaad-majeed.github.io

Personal portfolio site for **Emaad Majeed** — maker & engineer.
Hosted on GitHub Pages, built with Jekyll.

**Live:** https://emaad-majeed.github.io

## Status

Minimal placeholder hub. Design and content are intentionally not built yet.

## Planned (later phases)

- **Design + content** — build the real UI and add projects (images, 3D models),
  all hosted on GitHub (this repo or linked repos).
- **Custom domain** — add a `CNAME` file, configure DNS, enable "Enforce HTTPS".

## Local preview (optional)

GitHub Pages builds this site automatically on push — no local setup required.
To preview locally you need Ruby 3.x + Bundler, then:

```sh
bundle install
bundle exec jekyll serve
```

## Structure

- `_config.yml` — site settings (no theme; custom layouts).
- `_layouts/default.html` — the page shell.
- `index.md` — the home page.
- `assets/css/style.css` — base styles.
