# Command: /import-project [slug]
# Trigger: /import-project [slug]
# Reads: projects/[slug].md, guidelines/*.md, career-profile/profile.md
# Writes: career-profile/profile.md, career-profile/skills.md
# Requires: setup complete, projects/[slug].md already written by user

**What it does:** Use when the user has written a complete `projects/[slug].md` themselves.
Skips the intake form. Handles wiki integration only.
Framing issues are warnings, not blockers — the user wrote this file deliberately.

1. Read all `.md` files in `guidelines/` and `projects/[slug].md`
2. Run a framing check — report findings as warnings only, not blockers:
   "Framing notes (optional to address before publishing): ..."
3. Ask: which category and where to place it. Wait for the answer.
4. Add the project to the correct section of `profile.md`
5. Add `-> [[slug]]` links to matching skill entries in Core Competencies
6. Check tags against the Skills section; propose new ones and confirm before writing
7. Report: what was linked, tags added, framing notes, any `[TBD]` markers found
