# Template: Technical Specification

**Phase:** 1 (Spec) — Write this after the Content Document
**Purpose:** All technical decisions, architecture, and design system. A developer should be able to build the project from this document alone.

## Why This Matters

Without a tech spec:
- You make decisions on the fly and forget why
- Two months later, you can't remember why you chose library X over Y
- AI tools generate inconsistent code because they don't know your conventions

With a tech spec:
- Every decision is documented with its reasoning
- New contributors understand the architecture immediately
- AI code generation follows your exact conventions

---

## Template

```markdown
# TECHNICAL SPECIFICATION — [PROJECT NAME]
## Version 1.0 | [Date]

**Companion Document:** CONTENT_DOCUMENT.md
**Purpose:** All technical decisions. No ambiguity.

---

## 1. TECH STACK DECISIONS

| Layer | Technology | Version | Why |
|-------|-----------|---------|-----|
| **Framework** | [FILL] | [FILL] | [FILL — why this over alternatives] |
| **Language** | [FILL] | [FILL] | [FILL] |
| **Styling** | [FILL] | [FILL] | [FILL] |
| **UI Components** | [FILL] | [FILL] | [FILL] |
| **Database** | [FILL or "None"] | [FILL] | [FILL] |
| **Auth** | [FILL or "None"] | [FILL] | [FILL] |
| **Hosting** | [FILL] | — | [FILL] |
| **Package Manager** | [FILL] | [FILL] | [FILL] |

### What We're NOT Using (and Why)

| Technology | Why Not |
|-----------|---------|
| [FILL] | [FILL — explain the rejection, not just "we don't need it"] |

---

## 2. PROJECT STRUCTURE

[Show the folder structure you'll use]

project-name/
├── public/
├── src/
│   ├── app/          # Routes/pages
│   ├── components/   # UI components
│   ├── lib/          # Utilities, data fetching
│   ├── types/        # TypeScript interfaces
│   ├── config/       # Site configuration
│   └── content/      # Content data files
├── .env.example
├── CLAUDE.md
└── package.json

---

## 3. PAGES & ROUTING

| Route | Type | Data Source | Notes |
|-------|------|------------|-------|
| `/` | Static | [FILL] | [FILL] |
| `/about` | Static | [FILL] | [FILL] |
| `/[slug]` | Dynamic (SSG) | [FILL] | Uses generateStaticParams |

---

## 4. COMPONENT ARCHITECTURE

### Server Components (default)
- [FILL — list components that render on the server]

### Client Components (interactive)
- [FILL — list components that need "use client"]
- [FILL — explain WHY each needs to be client-side]

### Data Flow
[Show how data moves from source to UI]

content files → lib/data-fetching → page.tsx → components

---

## 5. DESIGN SYSTEM

### Colors

| Token | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| Primary | [FILL — hex] | [FILL — hex] | Buttons, links, accents |
| Background | [FILL] | [FILL] | Page background |
| Foreground | [FILL] | [FILL] | Body text |
| Muted | [FILL] | [FILL] | Secondary text, borders |

### Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| Headings | [FILL] | [FILL] | [FILL] |
| Body | [FILL] | [FILL] | [FILL] |
| Code | [FILL] | [FILL] | [FILL] |

### Spacing
- Section padding: [FILL — e.g., `py-16 md:py-24`]
- Container max-width: [FILL — e.g., `max-w-6xl mx-auto px-4`]

---

## 6. ARCHITECTURE DECISION RECORDS (ADRs)

Write an ADR for any decision where reasonable engineers could disagree.

### ADR-001: [Decision Title]
- **Status:** Accepted
- **Context:** [What problem are we solving?]
- **Decision:** [What did we choose?]
- **Alternatives Considered:** [What else did we evaluate?]
- **Consequences:** [What are the trade-offs?]

### ADR-002: [Decision Title]
[Repeat for each significant decision]

---

## 7. ENVIRONMENT VARIABLES

| Variable | Purpose | Required | Example |
|----------|---------|----------|---------|
| [FILL] | [FILL] | Yes/No | [FILL — no real values] |

---

## 8. BUILD PHASES

### Phase 1: MVP
- [FILL — what ships first]
- Goal: [FILL]

### Phase 2: Polish
- [FILL — what comes next]
- Goal: [FILL]

### Phase 3: Growth
- [FILL — future enhancements]
- Goal: [FILL]

---

## 9. COMMANDS

[List every command a developer needs]

[package-manager] install     # Install dependencies
[package-manager] dev         # Dev server
[package-manager] build       # Production build
[package-manager] lint        # Linting
[package-manager] type-check  # TypeScript check
```

---

## Tips

- **"What We're NOT Using" is as important as what you are using.** It prevents someone from adding a database when you deliberately chose not to have one.
- **Write ADRs for trade-offs, not obvious choices.** You don't need an ADR for "use TypeScript" — you need one for "use MDX instead of a CMS."
- **Include version numbers.** "Next.js" is vague. "Next.js 16.x" is precise and prevents breaking changes during the build.
- **Design system values must be exact.** Don't write "blue" — write `#1E40AF`. Don't write "large padding" — write `py-16 md:py-24`.
- **Build phases set expectations.** Phase 1 is what you ship. Phase 2 is what you polish. Phase 3 is what you dream about.

## Real Example

See the safdarayub.dev portfolio's `PORTFOLIO_TECHNICAL_SPEC.md` — it has 18 sections covering every decision in the build.
