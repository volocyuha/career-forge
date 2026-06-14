# AGENTS.md — Career Forge

AI operator instructions. Read this file first, then read `career-profile/profile.md`
for person-specific context and output constraints.

> **Tool compatibility**
> Follows the `AGENTS.md` convention supported by OpenAI Codex and others.
> Claude Code users: rename or symlink to `CLAUDE.md` if your setup requires it.
> Cursor, Windsurf, and others: consult your tool's docs for agent instruction file names.

---

## What This Repo Is

Career Forge is an AI-powered career strategy system for professionals in IT,
game development, and other fields. It transforms projects, skills, achievements,
and lessons learned into a clear career roadmap, portfolio evidence, and interview-ready stories.

```
career-profile/profile.md        <- master index and source of truth
career-profile/current-role.md   <- current strengths, weaknesses, constraints
career-profile/target-role.md    <- target role requirements and success criteria
career-profile/strategy.md       <- concrete plan: projects, positioning, timeline
career-profile/skills.md         <- skill matrix with evidence levels
gap-analysis/[role]-gap.md       <- evidence gaps between current and target
interview-prep/star-stories.md   <- STAR stories from real project evidence
projects/*.md                    <- case studies, one page per project
prompts/*.md                     <- reusable AI prompt files
guidelines/                      <- drop any ruleset guide here; all .md files applied automatically
outputs/                         <- generated CVs, cover letters, portfolio cases
commands/                        <- full procedure for each command (load only when needed)
commands/setup.md                <- setup guide, question bank, and status tracker
new-project.md                   <- intake form, fill before running /add-project
```

---

## File Conventions

**Frontmatter** — flat key: value pairs, no YAML block scalars.

**Wikilinks** — `[[slug]]` format, matching filename without `.md`.

**Tags** — free-form discipline names. The Skills section of `profile.md` lists current tags,
but new ones can be added when a project introduces an unlisted skill. Any new tag must also be
added to the Skills section of `profile.md` with a description and project link.

**Guidelines folder** — before any write or review operation, read all `.md` files
in `guidelines/`. Each file is an operative ruleset. Apply all of them. Each guidelines
file opens with a `# Purpose:` line describing what it governs.

**Project filenames** — lowercase, hyphenated, matching the `slug` frontmatter field.

**Output filenames** — `outputs/cv-[studio]-[YYYY-MM-DD].md` and `outputs/cover-[studio]-[YYYY-MM-DD].md`.

**Command files** — each command's full procedure lives in `commands/[command-name].md`.
Load the relevant file when a command is invoked. Do not load all command files at once.

---

## First-Run Detection

At the start of every session, before doing anything else, check whether `profile.md`
contains `[YOUR NAME]` or any `[YOUR` placeholder text.

If placeholders are found: the repository has not been set up. Do not run any other command.
Read `commands/setup.md` and follow the AI Instructions for Setup section there.
Greet the user and offer the two setup options (CV/portfolio extraction or guided interview).

If no placeholders are found: the repository is set up. Proceed normally.
(Delete this block from AGENTS.md after successful setup.)

---

## Commands

When a command is invoked, read `commands/[command-name].md` for the full procedure.

| Command | File | What it does |
|---|---|---|
| `/setup` | `commands/setup.md` | Initialize the knowledge base from CV or guided interview |
| `/cleanup-setup` | `commands/cleanup-setup.md` | Strip setup scaffolding after setup completes |
| `/add-project` | `commands/add-project.md` | Process new-project.md into a project case study |
| `/import-project [slug]` | `commands/import-project.md` | Wire a self-written project page into the wiki |
| `/generate` | `commands/generate.md` | Generate a tailored CV and cover letter |
| `/review [slug]` | `commands/review.md` | Audit a project page against all active guidelines |
| `/interview [role]` | `commands/interview.md` | Generate mock interview questions and model answers |
| `/ats` | `commands/ats.md` | ATS keyword gap and formatting analysis |
| `/gap` | `commands/gap.md` | Gap analysis between current evidence and target role |
| `/strategy` | `commands/strategy.md` | Generate or update the career strategy document |
| `/rebuild-skills` | `commands/rebuild-skills.md` | Regenerate evidence-tracker/skills.md from project pages |
| `/link-skills [slug]` | `commands/link-skills.md` | Sync a project's skills into profile.md and skills.md |
| `/lint` | `commands/lint.md` | Health-check the whole wiki |
| `/profile-check` | `commands/profile-check.md` | Audit career profile for completeness and consistency |
| `/snapshot` | `commands/snapshot.md` | Quick overview of current state and next action |

---

## What the AI Must Not Do

- Invent experience, skills, outcomes, or metrics not in the wiki
- Add skills to `profile.md` without a project page to evidence them
- Edit any file during `/lint` without explicit user approval
- Modify Outcome sections of existing pages without confirmation
- Change the elevator pitch or positioning statement without being asked
- Use em dashes or negations anywhere in generated output
- Proceed with `/add-project` while framing issues are unresolved
- Load all command files at once — load only the file for the command being run
