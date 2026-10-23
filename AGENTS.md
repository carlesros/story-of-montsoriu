# AGENTS.md - The Story of Montsoriu

Agent routing, project overview, and guidelines for AI agents working in this repository.

---

## 1. Project Overview

- **Project Name:** The Story of Montsoriu
- **Type:** Digital Book & Static Website
- **Framework:** [Eleventy (11ty)](https://www.11ty.dev/) (v3.x)
- **Narrative:** The real-life story of **Montsoriu**, a cat found near Montsoriu Castle in Catalonia. Chapters are narrated from her sensory, first-person feline perspective.

---

## 2. Session Routing Instructions

Depending on the primary goal of the current session, consult the relevant guide:

### A. Narrative & Chapter Editing Sessions
When writing, editing, reviewing, or formatting chapter text:
👉 **Read and follow [NARRATIVE.md](file:///c:/Users/carle/Documents/story-of-montsoriu/NARRATIVE.md)**
- **Contains:** Character voice and feline POV rules, sensory storytelling principles, chapter conventions, and the living **Lexicon & Worldview Glossary** (how Montsoriu refers to humans, vehicles, nature, etc.).

### B. Website & Technical Development Sessions
When modifying templates, CSS styling, responsive layout, images, or build configuration:
👉 **Read and follow [WEBSITE.md](file:///c:/Users/carle/Documents/story-of-montsoriu/WEBSITE.md)**
- **Contains:** Eleventy architecture, Nunjucks layouts in `_includes/`, CSS typography and reading design rules, frontmatter schema, and build/dev server workflows.

---

## 3. Repository Structure

```text
story-of-montsoriu/
├── AGENTS.md                     # Central router & project overview (this file)
├── NARRATIVE.md                  # Narrative guide, voice rules & vocabulary lexicon
├── WEBSITE.md                    # Eleventy architecture, UI/CSS guidelines & build workflow
├── .eleventy.js                  # Eleventy configuration
├── .eleventyignore               # Files excluded from the static build
├── package.json                  # Dependencies & npm scripts
├── index.md                      # Book cover & introduction
├── chapter-*.md                  # Individual published chapter files
├── drafts/                       # Historical chapter drafts (excluded from build)
├── _includes/                    # Nunjucks layouts and partials
│   ├── cover.njk
│   ├── chapter.njk
│   └── partials/
├── css/                          # Stylesheets
├── images/                       # Media, photos, and chapter cover art
└── _site/                        # Generated output directory
```

---

## 4. Universal Rules for All Sessions

1. **Preserve Content Integrity:** Never overwrite, delete, or summarize away narrative passages unless explicitly requested by the author.
2. **Verify Changes:** 
   - If editing templates or web code, run `npm run build` to confirm the site compiles cleanly.
   - If editing narrative, ensure frontmatter metadata and file naming match the project conventions.
