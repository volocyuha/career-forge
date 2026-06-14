# Command: /gap [optional: target role]
# Trigger: /gap  or  /gap position-name
# Reads: career-profile/profile.md, career-profile/skills.md, career-profile/current-role.md, all projects/*.md, career-profile/target-role.md
# Writes: gap-analysis/[role]-gap.md (on user confirmation)
# Requires: setup complete

**What it does:** Compares current wiki evidence against the requirements of a target role.
Identifies missing evidence, underweighted skills, and suggests concrete next steps.

If no target role is passed, reads `gap_target` from the Identity section of `profile.md`.
**Example:** `/gap` (uses profile gap_target)
**Example:** `/gap technical-narrative-designer`

1. Read `profile.md`, `skills.md`, `current-role.md`,
   and all project pages
2. Read the relevant file `target-role.md` for the specified role.
   If no file exists for that role, derive requirements from common industry expectations
   and note that a target-role file is missing.
3. Build a gap report in four sections:

   **Current position**
   Summary of current evidence level per relevant skill, drawn from `skills.md`.
   Format: Skill | Current Evidence | Confidence

   **Missing evidence**
   Skills required for the target role with no current project evidence, or only Low evidence.
   For each: what evidence is missing and why it matters for this role.
   Format: Skill | Required level | Current level | Impact

   **Weak evidence**
   Skills present but at a lower evidence level than the role typically requires.
   Format: Skill | Current evidence | Required evidence | What would close the gap

   **Suggested portfolio projects**
   3-5 concrete project ideas that would close the most important gaps.
   For each: what to build, which skills it would evidence, realistic evidence level achievable,
   and approximate scope (weekend / 1 month / 3 months).

4. End with a priority order: which gap to close first and why
5. Ask the user whether to save the report to `gap-analysis/[role]-gap.md`
