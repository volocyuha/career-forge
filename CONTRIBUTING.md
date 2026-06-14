# Contributing to Career Forge

Thanks for your interest in improving Career Forge.
This is a small open-source project — contributions that make it more useful for real people are welcome.

---

## What's Useful to Contribute

**High value:**
- Target role templates for specific disciplines
- Anonymized gap analysis examples showing real before/after
- Anonymized project case studies (real structure, fictional details)
- Career strategy examples for different role transitions
- Corrections to command procedures in `commands/`
- Compatibility notes for AI tools not yet listed

**Also welcome:**
- Typo and grammar fixes
- Clarity improvements to templates and guides
- Additional guidelines files for specific fields or industries
- Improvements to `guidelines/it-portfolio-rules.md` or `guidelines/gamedev-portfolio-rules.md`

**Not a good fit:**
- Adding new commands without a clear use case and full procedure
- Changes to core architecture without prior discussion
- AI-generated content submitted as examples

---

## How to Submit

1. Fork the repo
2. Create a branch: `git checkout -b your-contribution-name`
3. Make your changes
4. Open a pull request with a short description of what you changed and why

For larger changes — new modules, structural changes, new command files — open an Issue first to discuss before building.

---

## File Conventions

Before contributing, read `AGENTS.md` File Conventions. Key rules:

- No em dashes anywhere
- No negations ("X isn't just Y", "X is more than Y")
- Command files must follow the header format: `# Command`, `# Trigger`, `# Reads`, `# Writes`, `# Requires`
- Template files keep `#>` instruction comments for user guidance
- All paths in command files use bare filenames in procedure steps; full paths go in the `# Reads` / `# Writes` header only

---

## Questions

Open an Issue or reach out via [volocyuha.com](https://volocyuha.com).
