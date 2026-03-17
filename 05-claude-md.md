# Template: CLAUDE.md

**Phase:** 2 (Design) — Write this after all spec documents are complete
**Purpose:** The master instruction file that Claude Code reads automatically at the start of every session. It's your project's persistent memory — no re-explaining, no context loss between sessions.

## What is CLAUDE.md?

When you open a project folder with Claude Code, it automatically reads `CLAUDE.md` from the project root. This means every conversation starts with full project context. You never have to say "we're using Next.js 16 with Tailwind" again — it's already loaded.

Think of it as **project documentation optimized for AI consumption.**

## What Makes a Good CLAUDE.md

- **Concise but complete.** Claude Code reads this every session — don't make it 50 pages. Aim for 1-3 pages.
- **Factual, not aspirational.** Describe what exists now, not what you hope to build someday.
- **Exact values, not vague descriptions.** Write `#1E40AF` not "blue". Write `pnpm` not "a package manager".
- **Points to source documents.** Instead of duplicating the full spec, reference it: "See TECH_SPEC.md §5 for design system."

---

## Template

```markdown
# CLAUDE.md

This file provides guidance to Claude Code when working with this codebase.

## Project Overview

[2-3 sentences: What is this? What stage is it at? Where is it deployed?]

## Tech Stack

- **Framework:** [Name + version]
- **Language:** [Name + version]
- **Styling:** [Name + version]
- **UI Components:** [Name]
- **Animations:** [Name + version, or "None"]
- **Database:** [Name, or "None — static site"]
- **Auth:** [Name, or "None"]
- **Package Manager:** [Name]
- **Deployment:** [Platform]

## Commands

[Every command a developer needs, with comments]

[pm] install          # Install dependencies
[pm] dev              # Dev server at localhost:3000
[pm] build            # Production build
[pm] lint             # Linting
[pm] type-check       # TypeScript check

## Architecture

### Data Flow

[Show how data moves through the system]

src/content/ → src/lib/ → page.tsx → components

### Rendering Strategy

[SSG, SSR, CSR, ISR — and why]

### Server vs Client Components

- **Server:** [List with reason]
- **Client:** [List with reason — what makes each one client-side]

### Key Types

- `src/types/[name].ts` — [Interface name and purpose]

## Content Source Documents

- **CONTENT_DOCUMENT.md** — All text content and copy
- **TECH_SPEC.md** — Technical decisions and architecture
- **WIREFRAMES.md** — Page layouts (desktop + mobile)
- **TASK_BREAKDOWN.md** — Build phases, milestones, and tasks

## Design System

- **Colors:** [Exact hex values for primary, background, foreground]
- **Fonts:** [Font names, how they're loaded]
- **Spacing:** [Section padding, container max-width]

## Environment Variables

[List each variable with purpose — no real values]

VARIABLE_NAME=description_here

## Key Conventions

- [Convention 1 — e.g., "All animations respect prefers-reduced-motion"]
- [Convention 2 — e.g., "ShadCN components in src/components/ui/ — don't manually edit"]
- [Convention 3 — e.g., "Git branching: main (production), dev (development)"]
```

---

## Tips

- **Update CLAUDE.md as the project evolves.** When you add a new page, update the architecture section. When you add a new convention, add it here.
- **"Current State" is powerful.** A line like "Phase 1 MVP complete. Next: Phase 2 (Blog + Polish)" tells Claude exactly where the project is.
- **Don't duplicate the spec.** Point to it. `CLAUDE.md` is a summary, not a copy.
- **Keep conventions actionable.** "Write clean code" is useless. "All animations use `whileInView` with `once: true`" is actionable.
- **Test it.** Open Claude Code in your project. If it understands your project context without you explaining anything, your CLAUDE.md is working.

## CLAUDE.md vs Other Docs

| Document | Audience | Detail Level | Updated |
|----------|----------|-------------|---------|
| CLAUDE.md | AI assistant | Summary | Every session |
| Tech Spec | Developers | Full detail | At milestones |
| Content Doc | Content writers | Full detail | When content changes |
| README.md | Public/GitHub | Overview | At releases |

CLAUDE.md is not your README. README is for humans on GitHub. CLAUDE.md is for your AI coding assistant.

## Real Example

See the safdarayub.dev portfolio's `CLAUDE.md` — it covers project overview, tech stack, commands, architecture, design system, environment variables, and conventions in ~100 lines.
