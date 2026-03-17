# Template: Wireframes

**Phase:** 1 (Spec) — Write this after the Content Document
**Purpose:** Text-based layouts showing where every element goes on every page, for both desktop and mobile.

## Why Text Wireframes?

- **Faster than Figma.** You can wireframe a full page in 5 minutes with text.
- **AI-readable.** Claude Code can read text wireframes directly and generate matching layouts. It can't read Figma files.
- **Version-controlled.** They live in your repo alongside your code and specs.
- **No design tool needed.** Anyone can create and read them.

---

## Template

```markdown
# WIREFRAMES — [PROJECT NAME]
## Text-Based Page Layouts | [Date]

**Legend:**
- `[ ]` = button
- `[===]` = input field
- `---` = horizontal line/separator
- `|` = column divider
- `← →` = horizontal arrangement
- Content in `CAPS` = section labels (not displayed text)

---

## SHARED: NAVBAR (All Pages)

### Desktop (>1024px)
┌──────────────────────────────────────────────────┐
│  Brand Name      Link1  Link2  Link3     [CTA]  │
└──────────────────────────────────────────────────┘
   ↑ Notes about behavior (sticky, blur, etc.)

### Mobile (<640px)
┌──────────────────────┐
│  Brand Name    [☰]   │
└──────────────────────┘
   ↑ Hamburger opens drawer:
   ┌────────────────┐
   │          [✕]   │
   │  Link1         │
   │  Link2         │
   │  Link3         │
   │  [CTA Button]  │
   └────────────────┘

---

## SHARED: FOOTER

┌──────────────────────────────────────────────────┐
│  Brand         Quick Links       Connect         │
│  Tagline       Link1             Social1         │
│                Link2             Social2         │
│                Link3             Social3         │
│                                                  │
│  © 2026 Name. All rights reserved.               │
└──────────────────────────────────────────────────┘

---

## PAGE: HOME

### Desktop
┌──────────────────────────────────────────────────┐
│                    NAVBAR                         │
├──────────────────────────────────────────────────┤
│                                                  │
│  HERO SECTION                                    │
│  ┌─────────────────────────┬──────────────┐      │
│  │ Headline text           │  Image/      │      │
│  │ Subheadline text        │  Visual      │      │
│  │ [CTA Button]            │              │      │
│  └─────────────────────────┴──────────────┘      │
│                                                  │
├──────────────────────────────────────────────────┤
│                                                  │
│  SECTION NAME                                    │
│  Section heading                                 │
│  ┌──────┐ ┌──────┐ ┌──────┐                     │
│  │Card 1│ │Card 2│ │Card 3│                      │
│  └──────┘ └──────┘ └──────┘                      │
│                                                  │
├──────────────────────────────────────────────────┤
│                    FOOTER                         │
└──────────────────────────────────────────────────┘

### Mobile
┌──────────────────────┐
│       NAVBAR         │
├──────────────────────┤
│                      │
│  Headline text       │
│  Subheadline text    │
│  [CTA Button]        │
│  Image/Visual        │
│                      │
├──────────────────────┤
│                      │
│  Section heading     │
│  ┌──────────────┐   │
│  │   Card 1     │   │
│  └──────────────┘   │
│  ┌──────────────┐   │
│  │   Card 2     │   │
│  └──────────────┘   │
│  ┌──────────────┐   │
│  │   Card 3     │   │
│  └──────────────┘   │
│                      │
├──────────────────────┤
│       FOOTER         │
└──────────────────────┘

---

## PAGE: [REPEAT FOR EACH PAGE]

[Same desktop + mobile format]

---

## FORMS

### Contact Form
┌──────────────────────────────────┐
│  Name    [===================]   │
│  Email   [===================]   │
│  Subject [===================]   │
│  Message [===================]   │
│           [===================]  │
│           [===================]  │
│                                  │
│  [Send Message]                  │
└──────────────────────────────────┘
```

---

## Tips

- **Always show both desktop and mobile.** Responsive issues are the #1 thing missed in planning.
- **Use arrows (↑) for behavioral notes.** "Sticky on scroll", "Fades in on scroll", "Opens modal on click" — these clarify what static wireframes can't show.
- **Don't overdesign.** Wireframes show *placement*, not visual design. Colors, fonts, and exact spacing belong in the Technical Spec's design system.
- **Include forms.** Every input field, button, and validation message should be in the wireframe.
- **Show empty/loading/error states** if they matter. What does a blog page look like with zero posts?

## Real Example

See the safdarayub.dev portfolio's `WIREFRAMES.md` — it covers navbar, footer, home, about, projects, blog, and contact pages with desktop and mobile layouts.
