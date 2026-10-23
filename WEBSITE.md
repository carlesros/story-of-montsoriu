# WEBSITE.md - Website Development & Architecture Guide

Instructions and technical guidelines for AI agents working on the website, templates, styling, and build setup for *The Story of Montsoriu*.

---

## 1. Technology Stack & Build Tools

- **Engine:** [Eleventy (11ty)](https://www.11ty.dev/) (v3.x)
- **Templating:** Nunjucks (`.njk`)
- **Styling:** Vanilla CSS (`css/`)
- **Image Optimization:** `@11ty/eleventy-img` transform plugin (configured in `.eleventy.js` to output AVIF/WebP)
- **Hosting / Deploy:** Static output in `_site/` (configured with `wrangler.jsonc` for Cloudflare Pages)

### Common Commands

- **Start Local Server:** `npm start` (runs `eleventy --serve`)
- **Production Build:** `npm run build` (runs `eleventy`)
- **Asset Passthrough:** Both `images/` and `css/` are copied directly to `_site/` by `.eleventy.js`.

---

## 2. Directory Structure

```text
story-of-montsoriu/
├── .eleventy.js                  # Eleventy configuration (passthroughs, filters, plugins)
├── .eleventyignore               # Files and directories excluded from the build
├── package.json                  # Dependencies and scripts
├── index.md                      # Book cover / introduction (uses cover.njk layout)
├── chapter-*.md                  # Individual chapter markdown files
├── css/                          # CSS stylesheets (e.g., modern responsive typography)
├── drafts/                       # Chapter drafts (ignored by Eleventy)
├── _includes/                    # Nunjucks layouts and partials
│   ├── cover.njk                 # Home/cover layout
│   ├── chapter.njk               # Chapter layout (header, nav, article content)
│   └── partials/                 # Modular layout partials (head, header, footer, etc.)
├── images/                       # Static media (photos, chapter cover art, favicon)
└── _site/                        # Generated output directory (build target)
```

---

## 3. Chapter Frontmatter (Technical Specs)

Every chapter markdown file must provide frontmatter parsed by Eleventy:

```markdown
---
layout: chapter.njk
title: "Determined to Live"
number: 1
date: 2018-09-14
location: "Near the castle Montsoriu"
cover: /images/capitol01/castell-sense-torra.jpg
prev: /
next: /chapter-2-slug/
---
```

- `layout`: Always `chapter.njk` for chapters, `cover.njk` for `index.md`.
- `date`: In ISO format (`YYYY-MM-DD`). Formatted via the custom filter `formatChapterDate` (e.g., "September 14, 2018").
- `prev` / `next`: Relative paths for seamless chapter-to-chapter navigation.

---

## 4. UI, Styling & Reading Experience

- **Reading-Focused Typography:**
  - Maintain optimal line length (60–75 characters per line) for long-form comfort.
  - Comfortable line height (`line-height: 1.6` to `1.8`) and distinct paragraph spacing.
  - Clear heading hierarchy and elegant serif or clean sans-serif editorial typefaces.
  - **Emphasis & Sound Effects:** Emphasized text (`.prose em`) is styled with medium-weight italic (`font-weight: 500`) and a warm accent hue (`--accent-gold-light` in dark mode, `--accent-gold-dark` in light mode); standalone auditory beats (`.prose p:has(> em:only-child)`) have enhanced sizing and spacing for clear readability.
- **Distraction-Free Layout:**
  - Keep the reading interface clean and uncluttered.
  - Chapter navigation (Next/Prev chapter, return to cover) should be accessible and non-intrusive.
- **Semantics & Accessibility:**
  - Use valid semantic HTML5 (`<header>`, `<main>`, `<article>`, `<nav>`, `<footer>`).
  - Provide descriptive `alt` attributes for images.
  - Ensure good color contrast and keyboard navigation support.
- **Modularity:**
  - Keep templates modular inside `_includes/` using Nunjucks partials (`{% include "partials/..." %}`).

---

## 5. Web Developer Workflow & Quality Checks

1. **Check Existing Templates:** Inspect `_includes/` and `css/` before adding new styles or layout blocks.
2. **Verify Builds:** Run `npm run build` to confirm no broken template references, bad frontmatter, or missing assets.
3. **Responsive Testing:** Verify reading view at mobile (375px), tablet (768px), and desktop (1200px) widths.
