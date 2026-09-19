# AGENTS.md - The Story of Montsoriu

Instructions and guidelines for AI agents working in this repository.

---

## 1. Project Overview

- **Project Name:** The Story of Montsoriu
- **Type:** Static Website / Digital Book
- **Framework:** [Eleventy (11ty)](https://www.11ty.dev/) (v3.x)
- **Concept:** An ongoing online book published as a static website where each chapter is a dedicated webpage.
- **Narrative:** The book narrates the real-life story and adventures of **Montsoriu**, a cat found near (and named after) the historic **Montsoriu Castle** in Catalonia — or rather, the cat who found her human companions there. The narrative captures her perspective, journey, survival, and daily life.

---

## 2. Technology Stack & Directory Structure

```text
story-of-montsoriu/
├── .eleventy.js                  # Eleventy configuration (passthrough copy, directories)
├── package.json                  # Dependencies and scripts
├── index.md                      # Book cover / introduction (uses cover.njk layout)
├── chapter-*.md                  # Individual chapter source files
├── _includes/                    # Nunjucks (.njk) templates and layouts
│   ├── cover.njk                 # Home/cover layout
│   └── chapter.njk               # Chapter layout (with header, navigation, and story content)
├── images/                       # Static media (photos, illustrations, chapter assets)
│   ├── capitol01/
│   ├── capitol02/
│   ├── portada.jpg
│   └── favicon.png
├── _site/                        # Generated output directory (build target)
└── AGENTS.md                     # Agent instructions (this file)
```

### Key Tools & Commands

- **Local Dev Server:** `npm start` (runs `eleventy --serve`)
- **Production Build:** `npm run build` (runs `eleventy`)
- **Passthrough Copy:** The `images/` directory is automatically copied directly to `_site/images/`.

---

## 3. Content Structure & Conventions

### Frontmatter Conventions

Each chapter markdown file should follow standard frontmatter conventions:

```markdown
---
layout: chapter.njk
title: "Chapter 1: Determined to Live"
date: 2018-09-14
location: Near the castle Montsoriu
prev: /                         # (or previous chapter path)
next: /chapter-2-slug/
---
```

### File Naming
- Chapters use kebab-case file names: `chapter-<number>-<slug>.md` (e.g., `chapter-1-determined-to-live.md`).
- Landing/cover page: `index.md`.

### Narrative Voice & Tone
- The story is written with emotional resonance, warmth, and attention to sensory details (smells, sounds, feelings), often capturing the world from the cat's perspective.
- When drafting, formatting, or editing text, maintain the author's authentic storytelling voice and respect original markdown punctuation and structure.

---

## 4. UI, Styling & Reading Experience

- **Reading-Focused Design:** Prioritize typography, readable line lengths (60–75 characters per line), comfortable line height, and distraction-free layouts suitable for long-form reading.
- **Navigation:** Ensure seamless chapter-to-chapter navigation (Next / Previous buttons, chapter index, return to cover).
- **Semantics & Accessibility:** Use valid semantic HTML5 (`<header>`, `<main>`, `<article>`, `<nav>`, `<footer>`) with descriptive headings and proper image alt text.
- **Templates:** Keep layouts modular in `_includes/` using Nunjucks (`.njk`).

---

## 5. Agent Workflow Guidelines

1. **Understand Before Modifying:** Check existing templates in `_includes/` and content files before adding new layouts or altering styles.
2. **Preserve Content Integrity:** Never overwrite or discard narrative text unless explicitly instructed.
3. **Verify Builds:** Ensure that additions (new chapters, templates, assets) build cleanly without broken Eleventy links or missing layouts.
