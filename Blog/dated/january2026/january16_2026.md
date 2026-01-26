[Work With Me](../resume_page.md) [Projects](../projects.md), [Blog](../../blog.md)

# January 16th, 2026

This week was mostly a mix of writing, course support work, and the usual background maintenance that comes with keeping research output moving forward. Nothing flashy, but a lot of the unglamorous “make it actually usable and presentable” work that tends to determine whether projects stay alive or quietly collapse.

If you’re a student browsing out of curiosity: this post is more of a weekly technical log than a tutorial, but you may still find some useful tools and workflow ideas.

---

## Writing (and rewriting)

* I currently have several papers in a “ready to submit once reviewed” state. They’re archived in my standard Nextcloud structure and waiting for final pass-through and submission decisions.
* This week included a lot of rewriting and editing work: tightening wording, cleaning up structure, improving clarity, and generally doing the part of research writing that actually makes it readable.
* I’m nearing the end of Chapter 2 of my thesis. My goal was to finish it today, but realistically I’m still in the final stretch of integration and cleanup.
* My thesis workflow is structured so that individual sections can compile as paper-style units for easier review, then get merged into the main thesis once they’re stable. It’s slower upfront, but it prevents the thesis from becoming one giant fragile document that breaks every time I touch it.

---

## What I Worked On (Technical)

This week’s technical work was mostly about tightening up tooling and improving the “pipeline” around writing and documentation:

### LaTeX structure + modular writing

* I’ve been restructuring parts of my thesis/paper content so it’s easier to maintain as a modular system (split into files, with consistent section layering).
* This makes it easier to review individual sections, reuse material across papers, and keep the overall document build sane as it grows.

### Figures and media handling

* I’ve been working on cleaning up and managing figure assets (images, diagrams, exported plots, etc.), including extracting still frames from video sources when needed for documentation.
* This is the sort of boring detail that matters a lot once you’re preparing papers and need consistent, reproducible figures rather than a folder of “final_final2.png” chaos.

### Citations and references

* I’ve been standardising citations for tools used in simulation and circuit work (including SPICE-related tooling), and generally tightening up reference formatting.
* This is one of those tasks that isn’t intellectually exciting, but it makes the final work look professional and reduces last-minute scrambling when submissions are due.

---

## ENEL 400 TA Duties

* This week marked the start of the semester. Teams had their first meetings and have started forming groups.
* Next week, teams will begin moving from early concepts into actual project definition, including required documentation and planning milestones.
* Teams looking to get ahead should start thinking about scope and time requirements now. The schedule doesn’t get more forgiving later, and most project pain comes from underestimating integration effort.

---

## Notes for Students: Tools That Actually Help

### Project management

* It’s worth learning at least one project planning tool properly.
* I’m a fan of Mermaid charts for Gantt-style planning because they’re lightweight, readable, and integrate nicely with documentation workflows.
* The catch is that Mermaid-based planning is manual. It only works if you actually keep it updated.
* Project management is not a one-time activity. It’s daily maintenance: tracking progress, updating assumptions, and making sure your plan still reflects reality.

### Version control (Git)

* Git is a baseline professional skill. It’s not just for software: it’s extremely useful for documentation, reports, design files, and team collaboration.
* If you’re working in a group and not using version control, you are eventually going to lose work, overwrite someone else’s work, or both.

### PCB design tools

If your project involves custom hardware, you’ll likely be doing PCB design. There are plenty of valid tool choices:

* **KiCad** (open-source, fully featured, widely used)
* **DipTrace** (my personal preference)
* **EasyEDA** (common for quick iteration and JLCPCB workflows)
* **Altium** (excellent, if you have access)

There isn’t a single correct choice. What matters is choosing something your team can use consistently without turning the CAD tool into the main obstacle.
