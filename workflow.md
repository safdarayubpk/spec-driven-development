# The Complete Workflow: 5 Phases

This document walks through the entire spec-driven development process from idea to deployed project. Each phase has a clear goal, inputs, outputs, and a checklist.

---

## Overview

```
IDEA → Phase 0: Interview → Phase 1: Spec → Phase 2: Design → Phase 3: Generate → Phase 4: Review
       (15-30 min)          (1-2 hours)     (30 min)          (days/weeks)         (ongoing)
```

The first three phases (0-2) happen before any code is written. They typically take 2-3 hours total but save 10x that in avoided rework.

---

## Phase 0: Discovery Interview

**Goal:** Extract everything from the project owner's head into structured information.

**Input:** A project idea ("I want to build a portfolio website")

**Process:**
1. Run through the structured questionnaire (see [00-discovery-interview.md](00-discovery-interview.md))
2. Cover all 5 categories: Goals, Content, Tech, Design, Scope
3. Save the raw answers — they're the foundation for everything

**Output:** Written answers to 20-24 questions

**If using Claude Code:**
```
"I want to build [project idea]. Interview me with structured questions
before we start building so you can generate spec documents."
```

### Checklist
- [ ] Goals and audience are clear
- [ ] Content inventory is complete (what exists, what's missing)
- [ ] Tech preferences are documented
- [ ] Design preferences are captured
- [ ] MVP scope is defined (what ships first vs later)
- [ ] Interview answers are saved

---

## Phase 1: Spec (Write 4 Documents)

**Goal:** Turn interview answers into precise specification documents.

**Input:** Interview answers from Phase 0

**Process:** Create these documents in order (each one informs the next):

### Document 1: Content Document
- Every word of text that appears in the project
- Page-by-page content, navigation items, footer text
- Assets checklist (images, PDFs, videos)
- SEO metadata per page
- See [01-content-document.md](01-content-document.md)

### Document 2: Technical Specification
- Tech stack with justifications
- Project structure
- Component architecture (server vs client)
- Design system (exact colors, fonts, spacing)
- Architecture Decision Records (ADRs)
- Environment variables
- Build phases
- See [02-technical-spec.md](02-technical-spec.md)

### Document 3: Wireframes
- Text-based layouts for every page
- Desktop AND mobile versions
- Navbar, footer, forms, empty states
- See [03-wireframes.md](03-wireframes.md)

### Document 4: Task Breakdown
- Milestones with numbered tasks
- Each task has clear instructions and output criteria
- Ordered by dependency
- See [04-task-breakdown.md](04-task-breakdown.md)

**Output:** 4 complete spec documents in the project root

### Checklist
- [ ] Content Document covers every page and component
- [ ] Assets checklist shows what's ready vs needed
- [ ] Tech Spec has stack decisions with reasons
- [ ] Tech Spec has "What We're NOT Using" section
- [ ] Design system has exact hex values, font names, spacing values
- [ ] ADRs exist for every debatable decision
- [ ] Wireframes show desktop AND mobile for every page
- [ ] Task Breakdown has milestones with numbered tasks
- [ ] Every task has an Output/done criteria
- [ ] Phase 1 (MVP) vs Phase 2 (Polish) scope is clear

---

## Phase 2: Design (Create CLAUDE.md)

**Goal:** Create the master instruction file that Claude Code reads every session.

**Input:** The 4 spec documents from Phase 1

**Process:**
1. Summarize the key information from all 4 documents
2. Focus on what Claude Code needs to know every session
3. Point to source documents for full details
4. Include exact commands, conventions, and current state
5. See [05-claude-md.md](05-claude-md.md)

**Output:** `CLAUDE.md` in the project root

**If using Claude Code:**
```
"Based on our spec documents, generate a CLAUDE.md file that summarizes
the project for AI-assisted development."
```

### Checklist
- [ ] Project overview states what this is and its current state
- [ ] Tech stack lists every technology with version
- [ ] Commands section has every dev command
- [ ] Architecture section shows data flow
- [ ] Design system has exact values (not "blue" but "#1E40AF")
- [ ] Content source documents are referenced
- [ ] Key conventions are actionable
- [ ] File is concise (1-3 pages, not 50)

---

## Phase 3: Generate (Build)

**Goal:** Write code guided by the spec documents.

**Input:** CLAUDE.md + 4 spec documents + Task Breakdown

**Process:**
1. Start each session — Claude Code auto-reads CLAUDE.md
2. Follow the Task Breakdown — "Let's work on Milestone 3, Task 3.2"
3. Reference spec documents for details — Claude reads Content Doc for exact copy, Tech Spec for architecture
4. Build milestone by milestone, task by task
5. Commit after each milestone

**Output:** Working code that matches the specs

### Per-Session Workflow
```
1. Open project → Claude Code reads CLAUDE.md automatically
2. Check Task Breakdown → Identify next task
3. Tell Claude: "Let's work on Task X.Y"
4. Claude reads relevant spec documents
5. Build → Test → Commit
6. Move to next task
```

### Checklist (Per Milestone)
- [ ] All tasks in the milestone are completed
- [ ] Code matches wireframe layouts
- [ ] Content matches Content Document (no invented text)
- [ ] Architecture follows Tech Spec decisions
- [ ] `build` completes without errors
- [ ] `lint` passes
- [ ] `type-check` passes
- [ ] Responsive design works (desktop + mobile)
- [ ] Committed with clear message

---

## Phase 4: Review

**Goal:** Verify the implementation matches the specifications.

**Input:** Built code + spec documents

**Process:**
1. After each milestone, review against the spec
2. Check: Does the content match the Content Document?
3. Check: Does the layout match the Wireframes?
4. Check: Does the architecture follow the Tech Spec?
5. Check: Do ADR decisions hold up in practice?
6. Deploy to preview environment and visually inspect

**Output:** Confirmed match between spec and implementation, or a list of adjustments

### Review Checklist
- [ ] Every page renders correctly on desktop
- [ ] Every page renders correctly on mobile
- [ ] All content matches the Content Document
- [ ] All interactions work (forms, filters, navigation)
- [ ] SEO metadata is correct (check with browser dev tools)
- [ ] Performance is acceptable (Lighthouse score)
- [ ] Accessibility basics pass (keyboard nav, screen reader, contrast)
- [ ] No console errors in production build

---

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Skipping the interview | You'll write specs based on assumptions, not facts |
| Content Document with placeholders | Write actual text, even rough drafts. "Lorem ipsum" doesn't help |
| Tech Spec without "Why" | Every decision needs a reason. Future-you will ask "why did I choose this?" |
| Wireframes for desktop only | 50%+ of traffic is mobile. Always wireframe both |
| Tasks that are too big | "Build the blog" is 8 tasks, not 1. Break it down |
| Not updating CLAUDE.md | After each phase, update the "Current State" line |
| Building features not in the spec | If it's not in the Task Breakdown, it's Phase 2 |

---

## Adapting for Different Project Types

### Portfolio / Landing Page
- Content Document is heaviest (lots of copy)
- Tech Spec is lighter (simpler architecture)
- 20-40 tasks typical

### SaaS / Web App
- Tech Spec is heaviest (database, auth, API design)
- More ADRs (many architectural decisions)
- 60-100+ tasks typical

### API / Backend Service
- Wireframes are minimal or replaced with API endpoint docs
- Tech Spec focuses on data models, endpoints, error handling
- Task Breakdown follows API-first approach

### Mobile App
- Wireframes focus on screens and navigation flow
- Tech Spec covers platform-specific decisions
- Task Breakdown may separate iOS/Android tasks

---

The workflow is the same regardless of project type. The weight of each document shifts, but the process doesn't change.
