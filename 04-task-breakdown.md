# Template: Task Breakdown

**Phase:** 1 (Spec) — Write this last (after Content, Tech Spec, and Wireframes)
**Purpose:** Break the entire build into ordered milestones with numbered tasks. Each task is small enough to complete in one session. You always know what to build next.

## Why Task Breakdowns Matter

- **Prevents scope creep.** If it's not in the task list, it doesn't get built in this phase.
- **Shows progress.** You can see exactly how far along you are.
- **Enables delegation.** Each task has clear inputs and outputs — anyone can pick one up.
- **Ordered by dependency.** Task 12 knows it needs Task 8 done first. No confusion.

---

## Template

```markdown
# TASK BREAKDOWN — [PROJECT NAME]
## Phase 1: [Phase Name] (MVP)

Each task is a single focused unit of work. Complete them in order —
later tasks depend on earlier ones.

---

## Milestone 1: [Name]
> Goal: [One sentence — what's true when this milestone is done?]

### Task 1.1 — [Task Name]
- [Step-by-step instructions]
- [What tools/commands to run]
- [Any dependencies on other tasks]
- **Output:** [How you know this task is done]

### Task 1.2 — [Task Name]
- [Instructions]
- **Output:** [Completion criteria]

### Task 1.3 — [Task Name]
- [Instructions]
- **Output:** [Completion criteria]

---

## Milestone 2: [Name]
> Goal: [What's true when this milestone is done?]

### Task 2.1 — [Task Name]
- [Instructions]
- **Depends on:** Task 1.x
- **Output:** [Completion criteria]

[Continue for each task...]

---

## Milestone 3: [Name]
> Goal: [What's true when this milestone is done?]

[Tasks...]

---

## Phase 2: [Phase Name] (Polish / Enhancement)

[Repeat milestone/task structure for later phases]

---

## Summary

| Milestone | Tasks | Goal |
|-----------|-------|------|
| 1. [Name] | 1.1–1.4 | [Goal] |
| 2. [Name] | 2.1–2.6 | [Goal] |
| 3. [Name] | 3.1–3.5 | [Goal] |
| **Total** | **[N] tasks** | |
```

---

## How to Break Down Tasks

### Good task size
- Can be completed in 15-60 minutes
- Has a clear "done" state
- Produces a visible or testable result

### Too big
- "Build the projects page" — this is 5-6 tasks (data model, card component, filter, detail page, responsive, etc.)

### Too small
- "Create the file" — combine with the actual implementation

### Example: Breaking down "Projects Page"

```
Task 4.1 — Define Project data model
- Create src/types/project.ts with Project interface
- Output: TypeScript interface with all fields

Task 4.2 — Add project content data
- Create src/content/projects/ with one file per project
- Use exact content from Content Document
- Output: All project data files exist

Task 4.3 — Build project data layer
- Create src/lib/projects.ts with query functions
- Output: getProjects(), getProjectBySlug() work

Task 4.4 — Build ProjectCard component
- Create src/components/projects/project-card.tsx
- Match wireframe layout
- Output: Card renders with project data

Task 4.5 — Build projects listing page
- Create src/app/projects/page.tsx
- Display all projects using ProjectCard
- Output: /projects shows all project cards

Task 4.6 — Build project detail page
- Create src/app/projects/[slug]/page.tsx
- Use generateStaticParams for SSG
- Output: /projects/[slug] shows full project details

Task 4.7 — Add project filtering
- Create ProjectFilter client component
- Filter by category or tech stack
- Output: Users can filter projects interactively
```

---

## Tips

- **Number tasks within milestones** (1.1, 1.2, 2.1, 2.2). This makes referencing easy: "Let's work on Task 3.4."
- **Every task has an Output line.** This is your definition of done. Without it, you don't know when to stop.
- **Dependencies should be obvious from order.** If Task 2.3 depends on Task 2.1, say so explicitly.
- **Phase 1 is what you ship. Phase 2 is what you polish.** Don't put nice-to-haves in Phase 1.
- **Count your tasks.** The safdarayub.dev build had 7 milestones, 42 tasks in Phase 1. That's a good size for a portfolio. A SaaS app might have 60-80 tasks.
- **Recount after changes.** If you add or remove tasks, update the summary table.

## Real Example

See the safdarayub.dev portfolio's `TASK_BREAKDOWN.md` — 7 milestones, 42 tasks, from project setup to deployment.
