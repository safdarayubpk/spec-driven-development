# Discovery Interview Answers — safdarayub.dev
## Reconstructed from the actual build conversation

These are the answers extracted during the discovery interview before building the portfolio. They became the raw material for all spec documents.

---

### Category 1: Goals & Audience

**Q: What are you building?**
A personal portfolio website to showcase my work as an AI Engineer and Full Stack Developer. It needs a blog, project showcases, and a contact form.

**Q: Who is the primary audience?**
Potential employers, collaborators, and the AI/tech community. People who want to see what I've built and potentially work with me.

**Q: What is the single most important thing this project should accomplish?**
Showcase my AI engineering projects — especially the Personal AI Employee (Platinum tier hackathon project) — in a professional, polished way.

**Q: What problem does this solve?**
I have 4 significant projects and a unique background (Air Force → AI Engineering) but no central place to present it all. LinkedIn isn't enough.

**Q: Similar projects or sites you admire?**
Clean developer portfolios with dark mode, project showcases with tech stack badges, and integrated blogs.

---

### Category 2: Content & Data

**Q: What content do you already have?**
- 4 completed projects with GitHub repos, live demos, and screenshots
- A resume PDF
- A profile photo and photo with PIAIC founder
- PIAIC AI certificate
- YouTube video demo of AI Video Generator
- Blog post ideas based on my projects

**Q: What content needs to be created?**
- Blog posts (5 planned for launch)
- Project descriptions and case studies
- About page narrative (Air Force to AI journey)
- Privacy policy

**Q: What are the main pages?**
- Home (hero, stats, featured projects, timeline, skills)
- About (story, education, skills detail, values)
- Projects (4 projects with filtering)
- Blog (MDX posts with tags)
- Contact (form with email integration)
- Privacy Policy

**Q: Will content change frequently?**
Mostly static. Blog will get new posts occasionally. Projects may be added over time.

**Q: Resume/bio ready?**
Yes — resume PDF exists. Bio covers: 23+ years Pakistan Air Force (retired), currently at PIAIC Air University Islamabad studying Agentic & Robotic AI Engineering.

---

### Category 3: Technical Preferences

**Q: Preferred tech stack?**
Next.js (already in my stack from other projects), TypeScript, Tailwind CSS. Want ShadCN UI for components. Framer Motion for animations.

**Q: Where will this be hosted?**
Vercel — free tier, automatic deployments, already familiar with it.

**Q: Need a database?**
No. Blog is MDX files, projects are hardcoded TypeScript, contact form just sends email. No user data storage needed.

**Q: Need user authentication?**
No. Fully public site.

**Q: Contact form or email integration?**
Yes — a contact form that sends emails. Using Resend (simple API, free tier).

---

### Category 4: Design & Experience

**Q: Light mode, dark mode, or both?**
Both, with dark mode as default.

**Q: Visual style?**
Professional/corporate. Not playful. This is for employers and collaborators.

**Q: Brand colors, fonts, logo?**
Corporate blue theme. Light: `#1E40AF` (Blue 800). Dark: `#3B82F6` (Blue 500) with deep navy background `#0B1120`. Inter font for everything. No logo — just my name.

**Q: How important are animations?**
Moderate — scroll-triggered fade-ins, count-up stats, staggered card appearances. Must respect `prefers-reduced-motion`. No heavy parallax or 3D.

**Q: What devices matter most?**
Equal priority desktop and mobile.

---

### Category 5: Scope & Timeline

**Q: What's the MVP?**
All 6 pages (Home, About, Projects, Blog, Contact, Privacy) with full content, working contact form, deployed on Vercel.

**Q: What can wait for later?**
RSS feed improvements, advanced analytics, OG image generation for blog posts, additional blog posts beyond the initial 5.

**Q: Hard deadlines?**
No hard deadline, but want to ship quickly. Phase 1 MVP should be complete and deployed.

**Q: Existing assets to reuse?**
- 4 project GitHub repos with README screenshots
- Profile photos in `pictures/` folder
- Resume PDF
- YouTube video link for AI Video Generator demo

---

## What Happened Next

These answers were used to generate:
1. `PORTFOLIO_CONTENT_DOCUMENT.md` (v2.1) — 13 sections, every page's content
2. `PORTFOLIO_TECHNICAL_SPEC.md` — 18 sections, all technical decisions
3. `WIREFRAMES.md` — Desktop + mobile layouts for all pages
4. `TASK_BREAKDOWN.md` — 7 milestones, 42 tasks
5. `CLAUDE.md` — Project memory file

The result: safdarayub.dev shipped as planned with zero major rewrites.
