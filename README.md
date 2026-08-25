# emaad-majeed.github.io

Personal portfolio for **Emaad Majeed**, aspiring industrial designer.
Jekyll, hosted on GitHub Pages.

**Live:** https://emaadmajeed.com

> Making changes with an AI assistant? Read [CLAUDE.md](CLAUDE.md) first. It
> covers the writing conventions, the front matter rules and the traps that
> are not obvious from the code.

## Structure

```
_config.yml            site settings, collection config, plugins
index.md               home page: Select Projects, All Projects, Press
about.md               bio, headshot, skills
404.html / 500.html    error pages
robots.txt             deliberately permissive
_layouts/              default (shell), project, page
_projects/*.md         one file per project (73 of them)
assets/css/style.css   all styles
assets/projects/<slug>/  images for that project
assets/about/          headshot
```

## Adding a project

Create `_projects/my-project.md`:

```yaml
---
title: "My Project"
year: "2025"
blurb: "One sentence, shown in the All Projects list."
---

Body copy in Markdown, written in first person.

![Alt text, which is also shown as a visible caption](/assets/projects/my-project/photo-01.jpg)
```

Put the images in `assets/projects/my-project/`. Two things to get right:

- **Quote the year.** `year: "2025"`, not `year: 2025`. Unquoted breaks the sort.
- **Alt text is displayed** as a caption under each image, so write it as one.

### Optional front matter

| Key | Effect |
|---|---|
| `featured: true` | Adds a card to Select Projects. Needs `thumb`, `featured_order`, `tagline`. |
| `thumb` | Card image. Should be 16:9 on a pure black background. |
| `featured_order` | Card position, ascending. |
| `tagline` | Short descriptor shown under the card on phones. |
| `hero` | Full width image under the title. Set `hero_w`, `hero_h`, `hero_alt` too. |
| `hero_portrait: true` | For tall photos, so they are not blown up. |
| `class: "wide"` | Numbered section headings, for design deck style pages. |
| `external` | Row links to an external URL instead of a project page. |

## Deploying

Push to `main`. GitHub Pages rebuilds automatically, usually in under a minute.

```bash
git add -A && git commit -m "..." && git push origin main
```

Then confirm it actually shipped, rather than assuming:

```bash
curl -s -o /dev/null -w "%{http_code}\n" https://emaadmajeed.com/
```

## Local preview (optional)

Not required, since GitHub Pages does the build. If you want it locally you
need Ruby and Bundler:

```bash
bundle install && bundle exec jekyll serve
```
