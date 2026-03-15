---
title: "Kyatt's Corner: Learning Polish Grammar as a Structured Course Website"
categories: [Coding, Project]
tags: [coding, project, nextjs, tailwindcss, typescript, mdx, polish, education]
---

# The problem
I finished a full YouTube series on Polish grammar and wanted a clean, structured way to present the content in text form. Video platforms are great for watching, but they are not ideal for quick reference, revision, or skimming key rules. I needed a dedicated site where every lesson lives as a searchable, well-organized page.

# How to Use
The site is built around a complete course outline and individual lesson pages.
Website available at: [https://kyattpl.github.io/learning-polish-grammar/](https://kyattpl.github.io/learning-polish-grammar/)

### Course Outline
1. Scroll the full list of lessons on the homepage.
2. Click any lesson to open its dedicated page.
3. Use the list to track your progress or revisit specific topics.

### Lesson Pages
1. Each lesson combines structured explanations, examples, and recap sections.
2. Lessons include clean typography for fast reading and review.
3. A built-in YouTube embed keeps the original video close at hand.

## Functionality

- **Full Course Outline**: A scrollable list of every lesson with direct links.
- **Lesson Pages**: Consistent structure with goals, grammar rules, examples, and recap.
- **MDX Content Pipeline**: Lessons are generated from transcripts and scripts, then published as MDX.
- **Schema Validation**: Metadata is validated so lessons render reliably.
- **Polish-Themed UI**: White and red palette inspired by the Polish flag.
- **Responsive Layout**: Optimized for mobile and desktop.

# Where to access it
Project available on GitHub: [https://github.com/KyattPL/learning-polish-grammar](https://github.com/KyattPL/learning-polish-grammar)
Website available at: [https://kyattpl.github.io/learning-polish-grammar/](https://kyattpl.github.io/learning-polish-grammar/)

# Use cases

- **Learning**: A structured text-first course that complements the videos.
- **Reference**: Quick lookup of grammar rules without scrubbing through video timelines.
- **Teaching**: A clean, shareable resource for students.
- **Portfolio**: A complete production-grade Next.js project with real content.

# Technical details

Built with **Next.js (App Router)** and **TypeScript**, with **Tailwind CSS** for styling and **MDX** for lesson content. The content pipeline reads local transcripts and scripts, generates structured MDX lesson pages, and validates metadata before build. The site is static-first for speed and reliability, and each lesson page includes rich formatting for examples and grammar notes.

