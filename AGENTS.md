# Working on this repo

Personal portfolio for Emaad Majeed. Jekyll, built and hosted by GitHub Pages,
served at https://emaadmajeed.com.

Read this before making changes. Most of what follows cannot be inferred from
the code, and several items will silently break the live site if ignored.

---

## Getting set up anywhere

```bash
git clone https://github.com/emaad-majeed/emaad-majeed.github.io.git
cd emaad-majeed.github.io
```

That is the whole setup. All images live in the repo, so a clone is complete.
There is no build step you need to run: GitHub Pages builds on push. Local
preview is optional and needs Ruby plus `bundle exec jekyll serve`.

**Do not hardcode a local path.** This repo has already moved around the
owner's Desktop once. Work from wherever it is checked out.

**Check your tools before assuming.** Image work in this repo has been done
with `sips` (macOS only). ImageMagick, ffmpeg and Python PIL were NOT installed
on the machine where most of this was built. On a new machine, verify what
exists before writing a conversion command:

```bash
which sips magick convert ffmpeg; python3 -c "import PIL" 2>&1 | tail -1
```

---

## Deploying

```bash
git add -A && git commit -m "..." && git push origin main
```

GitHub Pages rebuilds automatically (workflow name: "pages build and
deployment"), normally in 30 to 60 seconds.

**Always verify. Never assume a push worked.**

```bash
gh api "repos/emaad-majeed/emaad-majeed.github.io/actions/runs?head_sha=$(git rev-parse HEAD)&per_page=1" \
  --jq '.workflow_runs[0] | "\(.status) \(.conclusion)"'
curl -s -o /dev/null -w "%{http_code}\n" https://emaadmajeed.com/
```

Two failure modes that have actually happened here:

1. **A build check that passes falsely.** If `git rev-parse HEAD` fails (see the
   macOS note at the bottom), the query runs with an empty SHA and returns the
   *previous* successful run. Confirm the commit SHA changed before trusting a
   green result.
2. **Committed but never pushed.** Work was once finished, committed locally and
   left unpushed by another session. The working tree looked clean and nothing
   was live. If a change is missing from the site, check
   `git log origin/main -1` against local `HEAD` first.

---

## Writing style, and it matters

These are the owner's standing preferences. They are consistent across all 73
project pages, so breaking them is visible.

**No dashes.** No em dashes, no en dashes, and no hyphens in prose. Write
compound words as separate words:

| Write this | Not this |
|---|---|
| laser cut, laser engraved | laser-cut |
| self watering | self-watering |
| tab and slot | tab-and-slot |
| end grain | end-grain |
| high speed | high-speed |

This covers body copy, `blurb`, `tagline`, alt text and headings. Hyphens
inside file paths, slugs and URLs are fine.

**First person on project pages.** "I designed the cabinet as flat panels."
The About page is third person, because it reads as a bio.

**Never narrate the image.** Describe the object, not the photograph. Say "The
finished panel has the meter openings cut and the switches installed", not
"The photo shows the finished panel". Every instance of that phrasing was
deliberately removed from the site once already.

**Never invent a specification.** This is the most important rule. Early drafts
of these pages were written from photographs and got materials, motor counts,
gear ratios and team numbers wrong. The owner corrected roughly 30 pages by
hand. Do not state RPM, wattage, dimensions, materials, team numbers or awards
unless the user told you or it is written somewhere in the repo. When in doubt,
describe what is visibly true and ask.

---

## Alt text becomes a visible caption

A script at the bottom of `_layouts/default.html` finds every image inside
`<article>`, wraps it in a `<figure>`, and copies its alt text into a visible
`<figcaption>` under the image.

So alt text is not just for screen readers here. It is the caption the reader
sees. Write it as one, and keep it accurate to that specific image.

---

## Front matter reference

Layout is assigned automatically by `_config.yml`; project files do not set it.

| Key | Files using it | Notes |
|---|---|---|
| `title` | 73 | Required. |
| `year` | 73 | Required. **Must be quoted**: `year: "2025"`. |
| `blurb` | 73 | Required. One sentence, shown in All Projects. |
| `featured` | 7 | `true` puts it in Select Projects. |
| `thumb` | 7 | Card image. Required when featured. |
| `featured_order` | 7 | Integer. Controls card order, ascending. |
| `tagline` | 7 | Short lowercase descriptor under the card on phones. |
| `hero` | 4 | Full width image below the title. |
| `hero_w` / `hero_h` | 4 | Pixel size. Reserves space, prevents layout shift. |
| `hero_alt` | 4 | Describes the hero. |
| `hero_portrait` | 1 | For tall photos. Centers at natural size, never upscales. |
| `class` | 2 | `"wide"` styles `h2` as numbered design deck section labels. |
| `external` | 2 | Row links to an external URL instead of a project page. |
| `category` | 59 | **Vestigial.** Left from home page sections that were removed. Unused. Harmless. |

### The year gotcha

`year` must be a quoted string. Unquoted, Jekyll reads it as an integer, and
sorting mixes integers with strings, which scrambles the All Projects order.
This has broken the build once. Check after any bulk edit:

```bash
grep -c '^year: [0-9]' _projects/*.md | grep -v ':0'   # any output is a bug
```

---

## Home page structure

`index.md` has three sections, all driven by Liquid.

**Select Projects** is a stacked single column of large images, one per row.
Cards come from `featured: true`, ordered by `featured_order`. On wide screens
the project name appears centred over the image on hover; on narrow screens
(40rem and below) the overlay is replaced by the title and tagline below the
image, and the images run edge to edge.

Current order: Tetris Arcade Machine, Pancake Robot Cooker, 3D Printed Plant
Pot, Override Robot, Pushback Small Bot 90 Gusset, Multistaging Water Rocket,
High Stakes Worlds Bot.

To add a card: set `featured: true`, `thumb`, `featured_order` and `tagline`
on the project. To reorder, renumber `featured_order`.

**All Projects** lists everything in the `projects` collection, sorted by year
descending. A project with `external:` links out and opens in a new tab
instead of going to its own page. That is how the two code repositories appear
in the list.

**Press** rows are written by hand directly in `index.md`, not generated.

---

## Images

Assets live at `assets/projects/<slug>/`. Naming in use: `photo-NN.jpg` for
build photos, `design-NN.png` and `render-NN.png` for CAD, `thumb.png` for the
card, `hero.png` for the page hero.

**Thumbnails must be 16:9 on a pure black background.** The page background is
`#000000`, and every current thumbnail is 2140x1204 with black corners, so the
subject appears to float with no visible frame. A thumbnail on a white or grey
background reads as an obvious rectangle and breaks the set. Verify a candidate
before using it.

**Heroes run full width and uncropped**, so send the whole image. Set `hero_w`
and `hero_h` to the real pixel size. Pages with a hero scroll to it on a fresh
visit, so the title sits just above the fold.

**Look at an image before publishing it.** A file handed over as a gusset
render turned out to be a screenshot of an app window containing personal
session names. It would have gone onto a public page indexed by every crawler.
Open the file. Confirm it is what its name claims.

---

## Site plumbing

- `robots.txt` is deliberately maximally permissive. Every crawler including AI
  crawlers is explicitly allowed. Do not add restrictions without being asked.
- `sitemap.xml` is generated by `jekyll-sitemap` (allowlisted on GitHub Pages).
  Currently 75 URLs. Error pages set `sitemap: false`.
- `404.html` works and is served for missing pages.
- `500.html` exists but **GitHub Pages will never serve it.** Static hosting
  gives no hook for server errors. It is there for a future host.
- Every project page ends with a byline from `_layouts/project.html`. The home
  and about pages end with a copyright line.
- `README.md` is in the `exclude:` list, so it is not published. `AGENTS.md`
  should stay excluded too.

---

## macOS specific trap

If `git` suddenly fails with "You have not agreed to the Xcode license
agreements", `xcode-select` is pointing at Xcode.app instead of the Command
Line Tools. The permanent fix needs a password (`sudo xcodebuild -license`), so
the user has to run it. A workaround that needs no privileges:

```bash
export DEVELOPER_DIR=/Library/Developer/CommandLineTools
```

This is specific to macOS machines with Xcode installed. It is irrelevant on
Linux or on a machine without Xcode.
