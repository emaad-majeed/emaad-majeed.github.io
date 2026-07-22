# emaad-majeed.github.io

Personal portfolio site for **Emaad Majeed** — maker & engineer.
Hosted on GitHub Pages, built with Jekyll.

**Live:** https://emaad-majeed.github.io

## Structure

- `_config.yml` — site settings (no theme; custom layouts).
- `index.md` — home page: intro + Projects list + Writing list.
- `_projects/*.md` — one Markdown file per project (front matter: `title`, `year`, `blurb`).
- `_blog/*.md` — one Markdown file per blog post.
- `about.md` — about + contact.
- `_layouts/` — `default` (shell), `project`, `post`, `page`.
- `assets/css/style.css` — all styles.
- `assets/projects/<slug>/` and `assets/blog/<slug>/` — images, stored in-repo.

## Adding a project

Create `_projects/my-project.md`:

```yaml
---
title: My Project
year: 2025
blurb: One-line description shown on the home page.
---

Write the project here in Markdown. Put images in
assets/projects/my-project/ and reference them as
![caption](/assets/projects/my-project/photo.jpg)
```

Push to `main` and GitHub Pages rebuilds automatically (~30–60s).

## Local preview (optional)

GitHub Pages builds on push — no local setup required. To preview locally
you need Ruby 3.x + Bundler, then `bundle install && bundle exec jekyll serve`.

## Planned (later)

- **Custom domain** — add a `CNAME` file, configure DNS, enable "Enforce HTTPS".
