# Changelog

All notable changes to Career Forge are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2025-06-14

Initial public release.

### Added

**Core system**
- `AGENTS.md` — AI operator instructions with first-run detection and command registry
- `WIKI_GUIDE.md` — human-facing system guide
- `new-project.md` — intake form for adding new projects

**Career profile module** (`career-profile/`)
- `profile.md` — master index and source of truth
- `current-role.md` — current strengths, weaknesses, and constraints
- `target-role.md` — target role requirements and success criteria
- `skills.md` — skill matrix with evidence levels
- `strategy.md` — career strategy document template

**Commands** (`commands/`) — 15 commands with full procedures
- `/setup` — initialize from CV or guided interview
- `/cleanup-setup` — strip scaffolding after setup
- `/add-project` — process new-project.md into a case study
- `/import-project` — wire a self-written project page into the system
- `/generate` — produce tailored CV and cover letter
- `/review` — audit a project page against guidelines
- `/interview` — mock interview with model answers and weak spot analysis
- `/ats` — ATS keyword gap and formatting analysis
- `/gap` — gap analysis between current evidence and target role
- `/strategy` — generate or update career strategy document
- `/rebuild-skills` — regenerate skills.md from project pages
- `/link-skills` — sync project skills into profile.md and skills.md
- `/profile-check` — audit career profile for completeness
- `/lint` — health-check the whole system
- `/snapshot` — quick overview and next recommended action

**Guidelines** (`guidelines/`)
- `gamedev-portfolio-rules.md` — portfolio writing rules for game development (source: gamedev.work/guidelines)
- `it-portfolio-rules.md` — portfolio writing rules for general IT

**Templates and examples**
- `projects/_PROJECT_TEMPLATE.md` — project case study template with evidence level scale
- `gap-analysis/technical-narrative-designer-gap.md` — example gap analysis
- `career-profile/target-role.md` — example target role file
- `interview-prep/star-stories.md` — STAR stories template

**Prompts** (`prompts/`) — 6 reusable AI prompt files
- `analyze-career-profile.md`
- `generate-gap-analysis.md`
- `build-career-strategy.md`
- `create-evidence-map.md`
- `prepare-interview-answers.md`
- `generate-portfolio-case-study.md`

**Repo files**
- `README.md`
- `LICENSE` (MIT)
- `CONTRIBUTING.md`
- `.gitignore`
