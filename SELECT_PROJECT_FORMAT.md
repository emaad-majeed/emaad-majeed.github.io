# Select Project Page Format

Use this guide when updating any featured project page in this portfolio. The
current [Tetris Arcade Machine](_projects/tetris-arcade-machine.md) page is the
working reference for this format.

Read `AGENTS.md` before editing. Its content, writing, image, and deployment
rules are mandatory.

## Goal

Featured project pages should read as concise design case studies. On desktop,
process text and related images form intentional side by side compositions. On
phones, preserve a simple sequence: text first, then related images in their
original order.

Use the page content to choose the image arrangement. Do not force every
section into the same composition if the image count or proportions do not fit.

## Content rules

- Write project page prose in first person.
- Never use dashes or hyphens in prose, captions, blurbs, taglines, headings,
  or alt text. File paths, URLs, CSS class names, and slugs are exceptions.
- Never invent a material, dimension, motor, ratio, award, team number, or
  other specification. Use only facts supplied by the user or already in the
  repository.
- Describe the object and work, never the photograph. Do not write "the photo
  shows."
- Treat every image alt value as a public caption. It must accurately describe
  that exact image.

## Front matter

Keep existing project front matter unless the user asks to change it.

- `year` must remain a quoted string, for example `year: "2025"`.
- Featured pages need `featured`, `thumb`, `featured_order`, and `tagline`.
- Add a page specific class alongside `wide` when custom layout CSS is needed,
  for example `class: "wide tetris-layout"`.
- Do not add `layout`. The collection assigns it automatically.

## Page structure

Use these two main headings unless the user requests a different structure:

```markdown
## 1. Process

...process steps...

## 2. Final Design

...final result and reflection...
```

Keep the introductory paragraph and the `Methods` and `Tools` facts block near
the top. Remove `Year` and `Team` from that block only when the user asks.

## Desktop layout pattern

Apply custom layouts only above `40rem`. At `40rem` and below, use a single
column layout with text followed by its images.

Begin with a page scoped base class rather than changing every project page:

```css
.example-layout .project-step {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 4rem;
  width: 100vw;
  margin: 1.25rem calc(50% - 50vw) 4.5rem;
  padding: 0 max(1.5rem, calc((100vw - 76rem) / 2));
}

@media (max-width: 40rem) {
  .example-layout .project-step {
    display: block;
    width: auto;
    margin: 1.25rem 0 4.5rem;
    padding: 0;
  }
}
```

Then choose one of these compositions for each process step.

### Two column pair

Use for a paragraph with one or more related images. Put `.step-copy` and
`.step-images` inside `.project-step`. Desktop places them side by side. The
mobile source order keeps the paragraph above the images.

### Four image wrap

Use for one text block and four images. Make a four column parent grid. Keep
the text and a three image row together in a three column content wrapper. Put
the fourth image in the right column. This prevents a tall right image from
pushing the three lower images far down the page.

```text
text, spanning three columns | side image
three smaller images beneath the text | side image continues
```

The Tetris CAD and electronics steps are working examples. Give each image an
explicit `grid-column` and `grid-row`; do not rely on automatic grid placement.

### Six image wrap

Use for a text block and six similarly sized images. Make a four column grid.
Place the text across two columns and two images in the other half. Place four
images in a second row. Mirror this arrangement on the next step when an
alternating left and right rhythm is desired.

```text
two images | text, spanning two columns
four smaller images beneath the full row
```

The Tetris fabrication step is the working example.

### Spacing between process steps

If the user asks for the large desktop separation used on Tetris, add it to the
complete step, never only its images or only its text:

```css
@media (min-width: 40.01rem) {
  .example-layout .spaced-step {
    margin-top: calc(1.25rem + 1.75in);
  }
}
```

This adds a 1.75 inch desktop offset while preserving the normal phone layout.

## Image markup

The default layout script turns Markdown only image paragraphs into figures and
visible captions. For custom grids, use an explicit figure so the class,
caption, and image size stay attached:

```html
<figure class="example-image">
  <img src="/assets/projects/example/photo-01.jpg" alt="Accurate caption for this image">
  <figcaption aria-hidden="true">Accurate caption for this image</figcaption>
</figure>
```

When Markdown appears inside a custom HTML `div`, include `markdown="1"` on
that `div`. Ensure nested containers have it too. Otherwise Jekyll can render
the Markdown image syntax as plain text.

Inspect every image before publishing. Do not publish screenshots, personal
information, or a wrongly named file.

## CSS rules

- Scope every custom selector to the page class. Do not alter the shared
  `.project-step` rules for one page.
- Keep image width at `100%` of its assigned grid cell. Choose image size by
  changing the number of grid columns, not by cropping an image.
- Set every custom image's `grid-column` and `grid-row` explicitly.
- In the phone media query, return image wrappers to `display: block` and give
  the first image a top margin. Keep the source image order intact.
- Do not use `transform` to create vertical spacing. Use margins so later
  content moves with the section and cannot overlap it.

## Safe workflow

1. Inspect the target project Markdown, referenced images, and current page
   specific CSS before editing.
2. Check image dimensions with `sips` before choosing a layout. Do not assume
   ImageMagick, ffmpeg, or Python imaging libraries are installed.
3. Edit only the target project page and its required scoped CSS. Use
   `apply_patch` for file changes.
4. Run `git diff --check`. Confirm that `year` values stay quoted.
5. Commit and push every completed user requested change unless the user says
   otherwise. Do not include unrelated working tree changes.
6. Verify the exact pushed commit through GitHub Pages. Confirm a successful
   Pages workflow and that `https://emaadmajeed.com/` returns HTTP 200.
7. When a desktop composition changes, inspect the live page at desktop width.
   Look for unexpected blank space, automatic grid placement in separate rows,
   overlap, and caption alignment.

For a normal update, stage exact paths, then commit and push:

```sh
git add _projects/example.md assets/css/style.css
git commit -m "Describe the project update"
git push origin main
```

Do not use `git add -A`. Other work may be present in the repository.
