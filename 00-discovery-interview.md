# Phase 0: Discovery Interview

The most critical step in the entire process. Before writing a single spec document, you run a structured interview to extract everything from the project owner's head into organized information.

## Why This Step Exists

Without the interview:
- You write specs based on what you *remember* to include
- You miss things and discover gaps mid-build
- The spec reflects what you *think* you want, not what you *actually* need

With the interview:
- Questions surface things you didn't think to mention
- Edge cases appear early ("What about mobile?", "Do you need a privacy policy?")
- The spec is complete because it was extracted systematically

## How to Run the Interview

**If using Claude Code or another AI assistant:**
Tell it: "I want to build [project idea]. Interview me before we start building — ask me structured questions so you can generate spec documents."

**If running it yourself or with a teammate:**
Go through the questions below. Write down answers. Don't skip the "boring" ones — they prevent surprises later.

**Time required:** 15-30 minutes

---

## The Questions

### Category 1: Goals & Audience

1. **What are you building?**
   Describe the project in 2-3 sentences. What does it do?

2. **Who is the primary audience?**
   Who will use this? Employers, clients, students, the general public?

3. **What is the single most important thing this project should accomplish?**
   If users only do one thing on your site/app, what should it be?

4. **What problem does this solve?**
   Why does this need to exist? What's the alternative without it?

5. **Are there similar projects or sites you admire?**
   Share 2-3 links or names. What do you like about them?

### Category 2: Content & Data

6. **What content do you already have?**
   Text, images, videos, PDFs, blog posts, project descriptions. List everything that exists today.

7. **What content needs to be created?**
   What's missing? Do you need to write copy, take screenshots, create assets?

8. **What are the main pages or sections?**
   List every page. For each one, describe what it shows in one sentence.

9. **Will content change frequently?**
   Is this mostly static (portfolio, landing page) or dynamic (blog, dashboard, e-commerce)?

10. **Do you have a resume, bio, or about-me text ready?**
    If not, what key points should it cover?

### Category 3: Technical Preferences

11. **Do you have a preferred tech stack?**
    Any frameworks, languages, or tools you already know or want to use?

12. **Where will this be hosted?**
    Vercel, Netlify, AWS, self-hosted? Any budget constraints?

13. **Do you need a database?**
    Does the project store user data, or is it mostly static content?

14. **Do you need user authentication?**
    Will users sign in? Or is this a public-facing site with no accounts?

15. **Do you need a contact form or email integration?**
    How should users reach you? Form, email link, social media?

### Category 4: Design & Experience

16. **Light mode, dark mode, or both?**
    Which is the default?

17. **What's the visual style?**
    Professional/corporate, creative/playful, minimal/clean, bold/dramatic?

18. **Do you have brand colors, fonts, or a logo?**
    Any existing branding to match?

19. **How important are animations?**
    None, subtle (fade-in), moderate (scroll animations), heavy (parallax, 3D)?

20. **What devices matter most?**
    Desktop-first, mobile-first, or equal priority?

### Category 5: Scope & Timeline

21. **What's the MVP?**
    If you could only ship 3-4 features/pages, which ones?

22. **What can wait for later phases?**
    Features that are nice-to-have but not essential for launch?

23. **Are there any hard deadlines?**
    Job applications, events, launches?

24. **What existing assets can you reuse?**
    Projects with GitHub repos, deployed apps, screenshots already taken?

---

## After the Interview

With answers in hand, you generate spec documents in this order:

1. **Content Document** (from Categories 1, 2, 5) — what the user sees
2. **Technical Spec** (from Categories 3, 4) — how you build it
3. **Wireframes** (from Categories 4, 8) — where things go
4. **Task Breakdown** (from Category 5) — build order
5. **CLAUDE.md** (summary of all above) — project memory

The interview answers become the raw material. The spec documents are the refined output.

---

## Tips

- **Don't edit answers during the interview.** Capture what the person says, refine later in the specs.
- **Ask follow-up questions.** If someone says "I want a projects page," ask: "How many projects? Do they have screenshots? Do you want filtering?"
- **It's OK to say "I don't know yet."** Mark it as a decision to make during the Design phase.
- **Save the interview answers.** They're useful context for anyone joining the project later.
- **Re-run for major pivots.** If the project scope changes significantly, do a mini-interview for the changed parts.
