# Career Forge

**Turn experience into a career strategy.**

Career Forge is a personal career knowledge base you build from real experience. The AI reads it and helps you turn that experience into a clear professional profile, targeted portfolio, and interview preparation.

---

## The Problem

You apply. No response. You apply again. Maybe a rejection, no reason given. You update the CV, rewrite the cover letter, and try again. Still nothing clear comes back.

The frustrating part is you don't know what's wrong. Is it the experience? The way it's presented? Are you targeting the wrong roles? Is there a skill gap you're not seeing? Without answers, you keep doing the same thing and hoping for a different result.

Most career tools help you present yourself better. But presentation isn't the problem when you don't know what you're actually missing.

Career Forge starts from a different place. Instead of polishing what you have, it helps you understand it — what you can actually prove, where the real gaps are, and what to do next. The AI doesn't generate advice from nothing. It reads your real experience and helps you build a strategy from it.

---

## How It Works

You build a knowledge base from your real experience — projects you shipped, decisions you made, outcomes you can prove. The AI reads it and helps you turn that into a coherent, evidence-based skill profile targeted at a specific role.

The system moves in one direction:

```
Note experience → Transform into skills → Show evidence → Reveal gaps
→ Build strategy → Shape portfolio → Prepare for interviews → Achieve goals
```

Your projects become proof of specific skills. That proof reveals gaps between where you are and where you want to go. The gaps define your strategy — what to build next, which roles to target, when you're actually ready to apply. The strategy shapes your portfolio, and the portfolio prepares you for interviews.

The more you put in, the more precisely it works.

---

## Who This Is For

Career Forge works for anyone whose career depends on demonstrable skills and a portfolio of real work.

**Game development:** Narrative Designers, Quest Designers, Technical Designers, Game Designers, Level Designers, Producers, Technical Artists

**General IT:** Software Engineers, Product Designers, UX Researchers, DevOps Engineers, Data Engineers, Product Managers, Engineering Managers

Especially useful if you are junior or mid-level and trying to grow deliberately — not just find a job, but understand where you are, where you're going, and what's actually in the way.

---

## Installation

No coding required. No configuration files to edit manually. The AI handles the rest.

**Step 1 — Get the files**

Click the green **Code** button on this page → **Download ZIP** → unzip it somewhere on your computer.

Or if you use Git:

```bash
git clone https://github.com/volocyuha/career-forge.git
```

**Step 2 — Open in your AI tool**

Open the `career-forge` folder in your AI coding assistant:

- **Claude Code** — run `claude` in the terminal inside the folder, or open it from the Claude Code interface. Rename `AGENTS.md` to `CLAUDE.md` first.
- **OpenAI Codex** — open the folder as a project. `AGENTS.md` is natively supported.
- **Cursor** — open the folder as a project. Add `AGENTS.md` to `.cursor/rules`.
- **Windsurf** — open the folder. Copy the contents of `AGENTS.md` into `.windsurfrules`.
- **Other tools** — open the folder and paste the contents of `AGENTS.md` as your system prompt.

**Step 3 — Run setup**

Type `/setup` in the chat with your AI assistant.
It will ask for your CV or walk you through a short interview.
The system builds your knowledge base from your answers.

---

## Modules

```
/
├── README.md                        ← you are here
├── AGENTS.md or CLAUDE.md           ← AI operator instructions and commands
├── WIKI_GUIDE.md                    ← human-facing system guide
├── new-project.md                   ← intake form for adding a new project
│
├── career-profile/
│   ├── current-role.md              ← who you are now: strengths, weaknesses, constraints
│   ├── profile.md                   ← master index and source of truth
│   ├── skills.md                    ← skill matrix with evidence levels per skill
│   ├── strategy.md                  ← concrete plan: projects, positioning, timeline
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
│   └── [all command procedures in separate files]
│
├── prompts/
│   └── [reusable AI prompt files]
│
├── guidelines/
│   ├── gamedev-portfolio-rules.md   ← portfolio writing rules (from gamedev.work/guidelines)
│   └── it-portfolio-rules.md        ← portfolio writing rules for general IT
│
└── outputs/
    └── [generated CVs, cover letters, portfolio cases, interview answers]
```

---

## Quick Start

1. Fork or clone this repo
2. Open the folder in your AI coding assistant (see tool compatibility below)
3. Run `/setup` — the AI will ask for your CV or walk you through an interview
4. Run `/snapshot` to see what to do next

Or fill in the files manually — start with `career-profile/profile.md`, then `career-profile/current-role.md`.

---

## Commands

| Command | What it does |
|---|---|
| `/setup` | Initialize the system from your CV or a guided interview |
| `/cleanup-setup` | Strip setup scaffolding after setup completes |
| `/add-project` | Process rough notes from `new-project.md` into a full case study |
| `/import-project [slug]` | Wire a project page you wrote yourself into the system |
| `/generate` | Produce a tailored CV and cover letter for a specific role |
| `/review [slug]` | Audit a project page against portfolio guidelines |
| `/interview [role]` | Generate mock interview questions, model answers, and weak spot analysis |
| `/ats` | Keyword gap and ATS formatting analysis against a job description |
| `/gap` | Gap analysis between current evidence and a target role |
| `/strategy` | Generate or update your career strategy document |
| `/rebuild-skills` | Regenerate `career-profile/skills.md` from all project pages |
| `/link-skills [slug]` | Sync a project's skills into `profile.md` and `skills.md` |
| `/profile-check` | Audit career profile for completeness and internal consistency |
| `/lint` | Health-check the whole system for broken links and missing content |
| `/snapshot` | Quick overview of what exists and what to do next |

---

## AI Tool Compatibility

| Tool | Setup |
|---|---|
| **Claude Code** | Rename or symlink `AGENTS.md` to `CLAUDE.md`, or use as-is |
| **OpenAI Codex** | `AGENTS.md` is natively supported |
| **Cursor** | Add to `.cursor/rules` or use as a context file |
| **Windsurf** | Copy contents to `.windsurfrules` or check your version's docs |
| **Other tools** | Paste `AGENTS.md` contents as your system/context prompt |

---

## AI Rules

The AI must:

1. Use only information present in the repository
2. Never invent experience, metrics, companies, or shipped results
3. Mark uncertain information as `[Needs confirmation]`
4. Separate strong evidence from weak evidence
5. Prioritize career strategy over generic advice
6. Recommend portfolio projects that close real skill gaps
7. Turn experience into evidence — not just polished text

---

## The Four Career Evidence Questions

Every project case study must answer:

1. What problem did I solve?
2. Why did I choose this solution?
3. What was the result?
4. What proves it?

---

## Credits

- Created by [Volodymyr Zubkov](https://volocyuha.com)
- Inspired by LLM-wiki pattern: [Andrej Karpathy](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
- Tested by [Narrative Designers Community](https://discord.gg/xCWpmgzU4b)
- Portfolio guidelines: [gamedev.work/guidelines](https://gamedev.work/guidelines)

Licensed under MIT.

---

## Contributing

Issues and PRs welcome. Particularly useful contributions:
- Target role templates for different disciplines
- Gap analysis examples
- Career strategy examples
- Anonymized project case studies
- Compatibility notes for other AI tools
