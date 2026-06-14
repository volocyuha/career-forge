# Career Forge — System Guide

Human-facing documentation. How to use this system, when to update each module, and what to publish.
For AI command procedures, see `AGENTS.md`.

---

## What This System Is

A career strategy framework for game development professionals.
Following the Karpathy LLM-wiki pattern: you build a structured knowledge base,
the AI reasons from it — not from generic templates.

```
Experience → Skills → Evidence → Gaps → Strategy → Portfolio → Interviews → Better decisions
```

---

## The Four Career Evidence Questions

Every project case study must answer all four:

1. What problem did I solve?
2. Why did I choose this solution?
3. What was the result?
4. What proves it?

If you can't answer all four, the case study isn't ready to use in applications.

---

## Module Overview

| Module | File | Purpose |
|---|---|---|
| Master index | `career-profile/profile.md` | Source of truth, links everything |
| Career profile | `career-profile/current-role.md` | Who you are now |
| Target role | `career-profile/target-role.md` | Where you want to go |
| Gap analysis | `gap-analysis/[role]-gap.md` | What's missing |
| Career strategy | `career-profile/strategy.md` | Concrete plan |
| Evidence tracker | `career-profile/skills.md` | Skill matrix with proof |
| Interview prep | `interview-prep/star-stories.md` | STAR stories from real evidence |
| Projects | `projects/*.md` | Case studies |
| Prompts | `prompts/*.md` | Reusable AI prompts |
| Commands | `commands/*.md` | All command rules |

---

## File Structure

```
/
├── README.md                        ← about this project and GIT description
├── AGENTS.md or CLAUDE.md           ← AI operator instructions and commands
├── WIKI_GUIDE.md                    ← human-facing system guide
├── new-project.md                   ← intake form for adding a new project
│
├── career-profile/
│   └── current-role.md              ← who you are now: strengths, weaknesses, constraints
│   └── profile.md                   ← master index and source of truth
│   └── skills.md                    ← skill matrix with evidence levels per skill
│   └── strategy.md                  ← concrete plan: projects, positioning, timeline
│   └── target-role.md               ← where you want to go and what it requires
│
├── gap-analysis/
│   └── [role-name]-gap.md           ← what's missing between current and target
│
├── interview-prep/
│   └── star-stories.md              ← STAR stories built from real project evidence
│
├── projects/
│   ├── _PROJECT_TEMPLATE.md         ← template for new case studies
│   └── [your project case studies]
│
├── commands/
│   └── [all command rules in separate files]
│
├── prompts/
│   └── [reusable AI prompt files]
│
├── guidelines/
│   └── gamedev-portfolio-rules.md   ← portfolio writing rules (from gamedev.work/guidelines)
│   └── it-portfolio-rules.md        ← portfolio writing rules for general IT
│
└── outputs/
    └── [generated CVs, cover letters, portfolio cases, interview answers]
```

---

## Commands

| Command | When to use |
|---|---|
| `/setup` | Initialize the system from your CV or a guided interview |
| `/cleanup-setup` | Strip setup scaffolding from filled files after setup is complete |
| `/add-project` | You have rough notes in `new-project.md` and want the AI to build the case study |
| `/import-project [slug]` | You wrote a project page yourself and want it wired into the wiki |
| `/generate` | You want a tailored CV and cover letter for a specific role |
| `/review [slug]` | You want an audit of a project page before publishing |
| `/interview [role]` | You want mock questions, model answers, and weak spot analysis |
| `/ats` | You want keyword gap and ATS formatting analysis against a job description |
| `/gap` | You want a gap analysis between current evidence and a target role |
| `/strategy` | You want to generate or update your career strategy document |
| `/profile-check` | You want an audit of your career profile for completeness |
| `/rebuild-skills` | You want to regenerate `career-profile/skills.md` from project pages |
| `/link-skills [slug]` | You want to sync a project's skills into `career-profile/profile.md` and `career-profile/skills.md` |
| `/lint` | You want a health check of the whole wiki |
| `/snapshot` | You want a quick overview of what exists and what to do next |

---

## Getting Started

If this is your first time, just run `/setup` and the AI will guide you through everything.

Or fill modules manually in this order:

1. `career-profile/profile.md` — replace all placeholders with real information
2. `career-profile/current-role.md` — be honest about strengths, weaknesses, constraints
3. `career-profile/target-role.md` — define where you're going
4. Run `/gap` — get your first gap analysis
5. Run `/strategy` — get your first career strategy
6. Add your first project: fill `new-project.md`, run `/add-project`
7. Run `/rebuild-skills` — generate `career-profile/skills.md`
8. Run `/snapshot` — see the full picture

---

## Adding a New Project

**From rough notes:**
1. Fill `new-project.md` — answer the four evidence questions first
2. Run `/add-project`
3. AI checks framing, guides you if anything needs work, creates the page
4. Fill any `[TBD]` markers — gaps only you can answer

**From a file you wrote yourself:**
1. Place your file in `projects/[slug].md`
2. Run `/import-project [slug]`
3. AI wires it into the wiki, flags framing notes as optional warnings

---

## Maintaining the System

**Update `career-profile/current-role.md` when:**
- Your job title or context changes
- You complete a significant project
- Your constraints change (location, availability, timeline)

**Update `career-profile/target-role.md` when:**
- Your target changes
- You do new research on role requirements

**Run `/gap` when:**
- You add a new project
- You close a gap (so the analysis reflects current state)
- You change your target role

**Run `/strategy` when:**
- Gap analysis changes significantly
- You complete a planned project
- You're ready to start applying

**Run `/rebuild-skills` when:**
- You add or significantly update a project page

---

## Adding Your Own Guidelines

The `guidelines/` folder is the AI's rulebook. Every `.md` file in it is read
automatically before any write or review operation.

The repo ships with two (delete anything irrelevant):
- `gamedev-portfolio-rules.md` — gamedev portfolio rules from gamedev.work/guidelines
- `it-portfolio-rules.md` — equivalent rules for general IT roles

To add your own: create any `.md` file in `guidelines/` and open it with:

```
# Purpose: [what this guide governs]
# Applies to: [which commands use it]
# Field: [your field or context]
```

Examples of guides you might add:
- `ats-rules.md` — ATS formatting rules for your target market
- `linkedin-rules.md` — rules for writing LinkedIn summaries and posts
- `cover-letter-rules.md` — company-specific tone or format rules
- `engineering-rules.md` — rules for a specific engineering discipline

Remove any guidelines file that doesn't apply to you. If you are not in gamedev,
delete or ignore `portfolio-rules.md`.

---

## Pre-Publish Checklist (Project Pages)

- [ ] Four evidence questions answered (problem / why / result / proof)
- [ ] At least one quantified or clearly observable outcome
- [ ] "What I'd do differently" is specific to this project
- [ ] `card_result` is a result statement, not a feature description
- [ ] `evidence_level` is set accurately in frontmatter
- [ ] No em dashes in the text
- [ ] No negations (X isn't just Y / X is more than Y)
- [ ] Framing is from the designer's perspective, not the game's
- [ ] `tags` match entries in the Skills section of `profile.md`
- [ ] `Skills Demonstrated` is linked from `profile.md` Core Competencies

---

## Publishing to Your Portfolio

Each `projects/*.md` maps to a portfolio page. Structure aligns with the odyssey-core template:

| Markdown | Portfolio element |
|---|---|
| `card_result` | Project card one-liner |
| `tags` | Filter tags |
| `## Overview` | Hero description |
| `## My Responsibilities` | Responsibilities section |
| `## Process & Design Decisions` | Case study body |
| `## Outcome` | Outcome metrics |
| `## Lessons Learned` | Lessons section |
