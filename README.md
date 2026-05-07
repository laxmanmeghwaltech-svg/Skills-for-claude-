<div align="center">

# 🧠 Skills for Claude

**A curated, production-ready library of SKILL.md files that extend Claude's capabilities across writing, content strategy, AI workflows, and multi-agent systems.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Compatible: Claude Code](https://img.shields.io/badge/Compatible-Claude%20Code-blueviolet)](https://claude.ai)
[![Compatible: Manus](https://img.shields.io/badge/Compatible-Manus-orange)](https://manus.im)
[![Skills](https://img.shields.io/badge/Skills-20%2B-brightgreen)](#skill-catalog)
[![Status: Active](https://img.shields.io/badge/Status-Active-success)](https://github.com/laxmanmeghwaltech-svg/Skills-for-claude-)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)](CONTRIBUTING.md.txt)

<br/>

> *"Most people treat AI like a vending machine — put in a prompt, get out a result.  
> Skills turn Claude into a system that already knows your brand, your voice, and your workflow."*

<br/>

[View Skill Catalog](#skill-catalog) · [Quick Start](#quick-start) · [How Skills Work](#how-skills-work) · [Contribute](#contributing)

</div>

---

## What This Repository Is

This is a personal, open collection of **SKILL.md files** — structured instruction documents that extend Claude (and Manus) with domain-specific expertise, repeatable workflows, and consistent behavior. Instead of re-explaining your context on every session, you load a skill once and Claude operates as a specialized agent for that domain.

Skills in this library cover:

- Removing AI writing patterns from human text
- Creating and formatting LinkedIn content
- Content strategy and copywriting frameworks
- Multi-agent coordination patterns
- Memory system design
- Social media scheduling via Typefully

These files were built through real production use — tested across hundreds of iterations and tens of thousands of impressions of published content.

---

## Skill Catalog

| Skill File | Domain | Version | Description |
|---|---|---|---|
| `SKILL.md` | Writing | 2.5.1 | **Humanizer** — removes 29 categories of AI writing patterns to make text sound natural |
| `copywriting-SKILL.md.txt` | Marketing | — | Conversion-focused copywriting for landing pages, headlines, and CTAs |
| `content-strategy-SKILL.md.txt` | Strategy | — | Topic clustering, content pillars, and editorial calendar planning |
| `linkedin-post-formatter.md.txt` | LinkedIn | — | Structures posts using PAS, AIDA, BAB, STAR, and SLAY frameworks |
| `linkedin-content-strategy-SKILL.md.txt` | LinkedIn | — | 30-day content plans across 21 post types and 37 bonus ideas |
| `social-content-SKILL.md.txt` | Social Media | — | Cross-platform content creation for LinkedIn, X, Instagram, and more |
| `typefully-SKILL.md.txt` | Automation | — | Draft, schedule, and manage posts via Typefully |
| `memory-systems-SKILL.md.txt` | Architecture | — | Persistent context and memory design for long-running AI sessions |
| `multi-agent-patterns-SKILL.md.txt` | Engineering | — | Coordination patterns for multi-agent Claude systems |
| `archetypes.md.txt` | Voice | — | Writing voice archetypes for brand consistency |

> Additional numbered skill variants (`SKILL.md (1–16).txt`) contain experimental or specialized extensions of the above.

---

## How Skills Work

A SKILL.md file is a structured Markdown document loaded into a Claude Project or passed as a system prompt. Claude reads the file and adopts the behavior, persona, tools, and processes defined within it — for the entire session.

```
┌─────────────────────────────────────────┐
│            Your Claude Project          │
│                                         │
│  ┌───────────────┐  ┌───────────────┐   │
│  │  SKILL.md     │  │  Your Files   │   │
│  │  (behavior)   │  │  (context)    │   │
│  └───────┬───────┘  └───────┬───────┘   │
│          └────────┬─────────┘           │
│                   ▼                     │
│          ┌────────────────┐             │
│          │  Claude Agent  │             │
│          │  (specialized) │             │
│          └────────────────┘             │
└─────────────────────────────────────────┘
```

**Without a skill:** Claude is a generalist. You re-explain your context, brand, and goals every session.

**With a skill:** Claude is a specialist. It knows your voice, your output format, your quality bar, and what to check before handing you anything.

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/laxmanmeghwaltech-svg/Skills-for-claude-.git
cd Skills-for-claude-
```

### 2. Pick a skill

Browse the [Skill Catalog](#skill-catalog) and identify the domain you need. For example, to humanize AI-generated text:

```
SKILL.md              ← Humanizer (remove AI writing patterns)
```

### 3. Load it into Claude

**Option A — Claude Projects (recommended)**

1. Open [claude.ai](https://claude.ai) and create or open a Project.
2. Upload the chosen `.md` or `.txt` skill file to the Project's knowledge base.
3. Claude will reference it automatically for every conversation in that Project.

**Option B — Claude Code / opencode**

Place the skill file in your working directory and reference it in your system prompt or directly read it with Claude Code's file tools:

```bash
# Example: load the humanizer skill into your Claude Code session
cat SKILL.md
```

**Option C — Manus**

Upload the skill file as a context document at the start of a Manus task session.

### 4. Invoke the skill

Most skills activate automatically once loaded. For the Humanizer specifically:

```
"Humanize this text: [paste your content]"

"Humanize this text. Here's a sample of my writing for voice matching: [sample]"

"Humanize this text. Use my writing style from [file path] as a reference."
```

---

## Featured Skill: Humanizer

The flagship skill in this collection. Based on [Wikipedia's "Signs of AI Writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) guide maintained by WikiProject AI Cleanup, it systematically detects and rewrites **29 categories** of AI writing patterns.

<details>
<summary><strong>View all 29 pattern categories</strong></summary>

**Content Patterns**
1. Undue emphasis on significance and legacy
2. Undue emphasis on notability and media coverage
3. Superficial analyses with `-ing` endings
4. Promotional and advertisement-like language
5. Vague attributions and weasel words
6. Formulaic "Challenges and Future Prospects" sections

**Language & Grammar Patterns**
7. Overused AI vocabulary words (`pivotal`, `tapestry`, `underscore`, `delve`, etc.)
8. Copula avoidance (`serves as`, `stands as`, `boasts`)
9. Negative parallelisms and tailing negations
10. Rule of three overuse
11. Elegant variation / synonym cycling
12. False ranges (`from X to Y`)
13. Passive voice and subjectless fragments

**Style Patterns**
14. Em dash overuse
15. Overuse of boldface
16. Inline-header vertical lists
17. Title case in headings
18. Emoji decoration in headings
19. Curly quotation marks

**Communication Patterns**
20. Collaborative artifacts (`"I hope this helps!"`, `"Let me know..."`)
21. Knowledge-cutoff disclaimers
22. Sycophantic/servile tone

**Filler & Hedging**
23. Filler phrases (`"In order to"`, `"Due to the fact that"`)
24. Excessive hedging
25. Generic positive conclusions
26. Hyphenated word pair overuse
27. Persuasive authority tropes (`"At its core"`, `"The real question is"`)
28. Signposting and announcements (`"Let's dive in"`, `"Here's what you need to know"`)
29. Fragmented headers

</details>

### Before / After Example

**Before (AI-generated):**
```
AI-assisted coding serves as an enduring testament to the transformative potential
of large language models, marking a pivotal moment in the evolution of software
development. In today's rapidly evolving technological landscape, these groundbreaking
tools—nestled at the intersection of research and practice—are reshaping how
engineers ideate, iterate, and deliver.
```

**After (Humanized):**
```
AI coding assistants can make you faster at the boring parts. Not everything.
Definitely not architecture.

They're great at boilerplate: config files, test scaffolding, repetitive refactors.
They're also great at sounding right while being wrong.
```

---

## Usage Examples

### Humanize a blog post

```
I have a blog post written by ChatGPT. Humanize it.
Keep the tone professional but make it sound like a real person wrote it.

[paste content]
```

### Match your personal writing voice

```
Humanize this text. Here's a sample of how I actually write:

[3–5 paragraphs of your own writing]

Now apply that voice to this AI draft:

[paste AI draft]
```

### Format a LinkedIn post

```
Using the LinkedIn post formatter skill, turn this idea into a post using the PAS framework.
Keep it under 200 words, mobile-formatted, with a strong hook.

Topic: Why most people are still at Level 1 with AI tools
```

### Plan 30 days of content

```
Using the LinkedIn content strategy skill, build a 30-day content calendar
for a creator focused on AI design systems and productivity workflows.
My three content pillars are: AI tools, personal branding, and systems thinking.
```

---

## Repository Structure

```
Skills-for-claude-/
│
├── SKILL.md                          # Humanizer v2.5.1 (primary skill, MIT)
│
├── Skill Variants (numbered)
│   ├── SKILL.md (1–16).txt           # Extended and experimental skill variants
│   └── SKILL.md.txt                  # Alternate format copy
│
├── Domain-Specific Skills
│   ├── copywriting-SKILL.md.txt
│   ├── content-strategy-SKILL.md.txt
│   ├── linkedin-post-formatter.md.txt
│   ├── linkedin-content-strategy-SKILL.md.txt
│   ├── social-content-SKILL.md.txt
│   ├── typefully-SKILL.md.txt
│   ├── memory-systems-SKILL.md.txt
│   └── multi-agent-patterns-SKILL.md.txt
│
├── Supporting Files
│   ├── archetypes.md.txt             # Voice archetypes reference
│   ├── sample-content.md.txt         # Sample content for testing
│   ├── LinkedIn posts.md             # Real published LinkedIn posts (examples)
│   ├── Untitled.md                   # Working drafts
│   └── humanizer-main.zip            # Packaged humanizer bundle
│
└── Meta
    ├── README.md                     # This file
    ├── README.md.txt                 # Alternate format
    ├── CONTRIBUTING.md.txt           # Contribution guidelines
    └── VERSIONS.md.txt               # Version history
```

---

## Design Philosophy

**Skills should be opinionated, not generic.** A skill file that hedges everything and covers every edge case usually produces mediocre output. The best skills make specific choices about quality, format, and process — and enforce them.

**Skills replace repetition, not judgment.** The goal is not to remove humans from the loop. It's to eliminate the part of the loop where you explain the same thing for the hundredth time. Judgment, editing, and taste stay with you.

**Documentation is the infrastructure.** Brand rules written down as hex codes and Tailwind classes produce consistent output. Vibes do not. Every skill in this library attempts to make implicit knowledge explicit.

**Iteration is how systems learn.** Many of these skills were shaped by dozens or hundreds of real outputs — not by writing the perfect prompt on the first try.

---

## Compatibility

| Platform | Supported | Notes |
|---|---|---|
| Claude Projects (claude.ai) | ✅ | Upload as knowledge base document |
| Claude Code | ✅ | Read via file tools or system prompt |
| opencode | ✅ | Pass as context file |
| Manus | ✅ | Upload as task context |
| ChatGPT / GPT-4 | ⚠️ Partial | Skill format is Claude-optimized; manual adaptation required |
| Gemini | ⚠️ Partial | Core instructions transfer; tool declarations do not |

---

## Contributing

Contributions are welcome. If you have a skill that solves a real, repeatable problem, this is the right place for it.

**What makes a good skill contribution:**

- Solves a specific domain problem, not a general one
- Has been tested on real tasks, not just designed theoretically
- Includes at least one before/after or usage example
- Follows the SKILL.md frontmatter format (name, version, description, license, compatibility)
- Is licensed under MIT or another permissive open-source license

**How to contribute:**

1. Fork the repository
2. Create a branch: `git checkout -b skill/your-skill-name`
3. Add your skill file following the naming convention: `your-skill-name-SKILL.md`
4. Open a pull request with a clear description of what the skill does and how you tested it
5. Include one or two real examples in the PR description

See [`CONTRIBUTING.md.txt`](CONTRIBUTING.md.txt) for full guidelines.

---

## Roadmap

| Status | Item |
|---|---|
| ✅ Done | Humanizer v2.5.1 (29-pattern AI writing detector) |
| ✅ Done | LinkedIn post formatter (PAS, AIDA, BAB, STAR, SLAY) |
| ✅ Done | Content strategy and copywriting skills |
| ✅ Done | Multi-agent coordination patterns |
| 🔄 In progress | Organized folder structure (skills by category) |
| 🔄 In progress | Skill version standardization across all files |
| 📋 Planned | Skill testing framework with real example inputs/outputs |
| 📋 Planned | AI design system skill (brand rules, HTML templates, QA agents) |
| 📋 Planned | Voice DNA builder skill (personal brand voice extraction) |
| 📋 Planned | Skill README generator (meta-skill that documents other skills) |

---

## License

The primary skill (`SKILL.md`) is released under the **MIT License**.  
See individual files for per-skill licensing — most are MIT.

```
MIT License

Copyright (c) 2025 Laxman Meghwal

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## Author

**Laxman Meghwal**

Building AI design systems and publishing the process openly.

- GitHub: [@laxmanmeghwaltech-svg](https://github.com/laxmanmeghwaltech-svg)
- LinkedIn: [Search "Laxman Meghwal" on LinkedIn](https://www.linkedin.com/search/results/all/?keywords=laxman+meghwal)

These skills were built in public — through iteration, failure, and the occasional 109-version infographic. The goal is to share what actually works, not a polished version of it.

---

<div align="center">

**If this saved you time, a ⭐ on the repo is appreciated.**  
**If you built something with it, open a PR — the library gets better when more people use it.**

</div>
