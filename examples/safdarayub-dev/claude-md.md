# CLAUDE.md — safdarayub.dev
## The actual CLAUDE.md used during the portfolio build

Below is the CLAUDE.md that was in the project root during development. It shows a real-world example of how to structure project instructions for AI-assisted development.

---

```markdown
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Safdar Ayub (safdarayub.dev) — an AI Engineer & Full Stack Developer.
This is a statically generated portfolio with blog, project showcases, and contact form.

**Current State:** Phase 1 MVP complete (all 7 milestones, 42 tasks). Live at safdarayub-dev.vercel.app.
Repo: github.com/safdarayubpk/safdarayub.dev. Next: Phase 2 (Blog + Polish).

## Raw Assets

Source assets are in `pictures/` at the project root. During build, selected images will be optimized
and copied to `public/images/` with clean filenames.

## Tech Stack

- **Framework:** Next.js 16 (App Router) with TypeScript
- **Styling:** Tailwind CSS 4 + ShadCN UI
- **Animations:** Framer Motion 11
- **Blog:** Local MDX files via next-mdx-remote + gray-matter
- **Contact Form:** React Hook Form + Zod validation → API route → Resend email service
- **Theme:** next-themes (dark mode default)
- **Package Manager:** pnpm
- **Deployment:** Vercel (SSG — all pages statically generated)

## Commands

pnpm install          # Install dependencies
pnpm dev              # Dev server at localhost:3000
pnpm build            # Production build
pnpm start            # Serve production build
pnpm lint             # ESLint via next lint
pnpm type-check       # TypeScript check (tsc --noEmit)

## Architecture

### Data Flow

src/content/projects/*.ts  →  src/lib/projects.ts  →  page.tsx  →  components
src/content/blog/*.mdx     →  src/lib/blog.ts      →  page.tsx  →  components

- Project data lives in TypeScript files under `src/content/projects/`
- Blog posts are MDX files under `src/content/blog/`
- Contact form submits to `src/app/api/contact/route.ts` which calls Resend API

### Rendering Strategy

All pages use Static Site Generation (SSG). Dynamic routes use `generateStaticParams`.
The contact form is the only client-interactive feature requiring an API route.

### Server vs Client Components

- **Client:** Navbar, Timeline, Project Filter, Contact Form, Share Buttons, Back to Top, Theme Toggle
- **Server:** Footer, Hero, Stats Bar, Project Card, Blog Post (MDX rendering)

### Key Types

- `src/types/project.ts` — Project interface
- `src/types/blog.ts` — BlogFrontmatter interface

## Content Source Documents

- **PORTFOLIO_CONTENT_DOCUMENT.md** — All text content
- **PORTFOLIO_TECHNICAL_SPEC.md** — All technical decisions
- **WIREFRAMES.md** — Text-based page layouts
- **TASK_BREAKDOWN.md** — 7 milestones, 42 ordered tasks

## Design System

- **Colors:** Corporate blue. Light: #1E40AF. Dark: #3B82F6, background #0B1120
- **Fonts:** Inter (headings + body), JetBrains Mono (code blocks, blog only)
- **Spacing:** Sections py-16 md:py-24. Container max-w-6xl mx-auto px-4 md:px-6

## Environment Variables

RESEND_API_KEY=re_xxxxxxxxxxxx
NEXT_PUBLIC_SITE_URL=https://safdarayub.dev
CONTACT_EMAIL=safdarayub@gmail.com

## Key Conventions

- All animations must respect `prefers-reduced-motion: reduce`
- Framer Motion scroll animations use `whileInView` with `once: true`
- ShadCN UI components in `src/components/ui/` — don't manually edit
- Git branching: main (production), dev (development), feature/* branches
```

---

## What Makes This CLAUDE.md Effective

1. **Current State line** — Claude knows the project is in Phase 1 complete, heading to Phase 2
2. **Exact versions** — "Next.js 16" not "Next.js", "Tailwind CSS 4" not "Tailwind"
3. **Data flow diagram** — Shows how content moves from source to UI
4. **Server vs Client split** — Claude knows which components need "use client"
5. **Points to source docs** — Doesn't duplicate the full spec, references it
6. **Exact design values** — `#1E40AF` not "blue", `py-16 md:py-24` not "large padding"
7. **Actionable conventions** — Not "write good code" but "use whileInView with once: true"
8. **~100 lines total** — Concise enough to load every session without overhead
