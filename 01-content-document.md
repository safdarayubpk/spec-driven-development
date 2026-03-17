# Template: Content Document

**Phase:** 1 (Spec) — Write this first
**Purpose:** Every word of text, copy, and content that will appear in your project. No content should ever be invented during development — it all comes from this document.

## Why Content Comes First

Most developers start with tech stack decisions. That's backwards. You need to know *what you're saying* before you decide *how to build it*. A portfolio with 4 projects needs a different architecture than one with 40. A blog-heavy site needs MDX; a static landing page doesn't.

Content drives architecture decisions, not the other way around.

## When to Write This

After the discovery interview (Phase 0). Use the interview answers about content, pages, audience, and goals as your raw material.

---

## Template

```markdown
# CONTENT DOCUMENT — [PROJECT NAME]
## Version 1.0 | [Date]

---

## TABLE OF CONTENTS

1. [Sitemap & Navigation](#1-sitemap--navigation)
2. [Page: Home](#2-page-home)
3. [Page: ...](#3-page-)
4. [Shared Components](#shared-components)
5. [Assets Checklist](#assets-checklist)
6. [SEO & Metadata](#seo--metadata)

---

## 1. SITEMAP & NAVIGATION

[List every page/route in your project as a tree]

example.com
├── / (Home)
├── /about
├── /projects
│   └── /projects/[slug]
├── /blog
│   └── /blog/[slug]
├── /contact
└── /404

### Navigation Items
- [List every link in the navbar]
- [Note which are buttons vs text links]

### Footer Links
- [List every link in the footer]

---

## 2. PAGE: HOME

### Hero Section
- **Headline:** [FILL — the main heading visitors see first]
- **Subheadline:** [FILL — supporting text, 1-2 sentences]
- **CTA Button:** [FILL — button text and where it links to]
- **Image/Visual:** [FILL — what image or graphic appears here]

### Section: [Name]
- **Heading:** [FILL]
- **Body text:** [FILL — exact copy]
- **Items/Cards:** [FILL — list each item with its text]

[Repeat for every section on the page]

---

## 3. PAGE: [REPEAT FOR EACH PAGE]

[Same structure as above — heading, body text, items, images]

---

## SHARED COMPONENTS

### Navbar
- Logo/brand text: [FILL]
- Links: [FILL — list with exact text]
- CTA button: [FILL — text and link]

### Footer
- Tagline: [FILL]
- Links: [FILL]
- Social icons: [FILL — which platforms]
- Copyright: [FILL]

---

## ASSETS CHECKLIST

List every image, PDF, video, and file needed:

| Asset | Source | Status | Notes |
|-------|--------|--------|-------|
| Profile headshot | [FILL] | Ready / Needed | [dimensions, format] |
| Project screenshot | [FILL] | Ready / Needed | [which project] |
| Resume PDF | [FILL] | Ready / Needed | [version] |
| Logo/favicon | [FILL] | Ready / Needed | |

---

## SEO & METADATA

### Global
- **Site title:** [FILL]
- **Site description:** [FILL — 150-160 chars for search results]
- **OG image:** [FILL — default social share image]

### Per Page
| Page | Title | Description |
|------|-------|-------------|
| Home | [FILL] | [FILL] |
| About | [FILL] | [FILL] |
| [etc.] | [FILL] | [FILL] |
```

---

## Tips

- **Be specific.** Don't write "some introductory text" — write the actual text. Even a rough draft is better than a placeholder.
- **Include dimensions and formats** for images. "Profile photo, 400x400px, PNG" prevents confusion later.
- **Mark what's ready vs what's needed** in the assets checklist. This tells you what's blocking the build.
- **Version the document.** When content changes, update the version and add a changelog entry at the top.
- **Don't mix technical decisions in here.** This document is about *what the user sees*, not how it's implemented. Tech decisions go in the Technical Spec.

## Real Example

See [examples/safdarayub-dev/content.md](examples/safdarayub-dev/content.md) for the content document from the safdarayub.dev portfolio build.
