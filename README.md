# Spec-Driven Development Guide

A practical, battle-tested framework for building software projects with AI-assisted development. Instead of diving straight into code, you write structured specifications first — then use those specs to generate accurate, consistent code.

## Origin Story

This guide was extracted from building [safdarayub.dev](https://safdarayub-dev.vercel.app) — a portfolio website that went from zero to deployed using this exact process. Every document, template, and example in this guide comes from that real build.

The approach combines military operations planning (23 years in Pakistan Air Force) with modern AI-assisted development. The core insight: **the time to discover problems is before execution, not during it.**

## Who This Is For

- Developers who want to build projects faster with fewer rewrites
- Teams using AI coding tools (Claude Code, Cursor, GitHub Copilot) and want better output
- Anyone who has started a project, gotten halfway through, and realized the foundation was wrong

## The 5-Phase Workflow

```
Phase 0: DISCOVERY INTERVIEW    ← Extract requirements through structured questions
Phase 1: SPEC                   ← Write 4 specification documents
Phase 2: DESIGN                 ← Create CLAUDE.md (project memory file)
Phase 3: GENERATE               ← Build with AI assistance, guided by specs
Phase 4: REVIEW                 ← Verify implementation matches specifications
```

## Files in This Guide

| File | Purpose |
|------|---------|
| [workflow.md](workflow.md) | The complete 5-phase process with checklists |
| [00-discovery-interview.md](00-discovery-interview.md) | Structured interview questionnaire (Phase 0) |
| [01-content-document.md](01-content-document.md) | Template: what the user sees (text, copy, content) |
| [02-technical-spec.md](02-technical-spec.md) | Template: how you build it (stack, architecture, ADRs) |
| [03-wireframes.md](03-wireframes.md) | Template: where things go (layouts, responsive design) |
| [04-task-breakdown.md](04-task-breakdown.md) | Template: build order (milestones, numbered tasks) |
| [05-claude-md.md](05-claude-md.md) | Template: CLAUDE.md project memory file |
| [examples/safdarayub-dev/](examples/safdarayub-dev/) | Real example from the portfolio build |

## Quick Start

1. Read [workflow.md](workflow.md) to understand the full process
2. Start with [00-discovery-interview.md](00-discovery-interview.md) for your next project
3. Use the templates (01-05) to create your spec documents
4. Reference the [examples/](examples/safdarayub-dev/) for a real-world implementation

## Key Principles

- **Content first, code second.** Know what you're building before choosing how to build it.
- **Document decisions, not just code.** When reasonable engineers could disagree, write an ADR.
- **30 minutes of planning saves hours of debugging.** Every time.
- **AI code generation is dramatically better with specs.** Vague prompts produce vague code. Precise specs produce precise implementations.
- **The interview is not optional.** It's the most critical step — it extracts what's in your head into structured information.

## Works With Any Stack

This guide is stack-agnostic. The process works whether you're building with:
- Next.js, React, Vue, Svelte
- Python, Go, Rust
- Mobile, desktop, CLI tools
- Any AI coding assistant or none at all

The specs are about *what* you build and *why*. The tech stack is just one decision within the spec.

## License

Free to use, share, and adapt. If it helps you build better software, that's the goal.

---

*Created by [Safdar Ayub](https://github.com/safdarayubpk) — AI Engineer & Full Stack Developer*
