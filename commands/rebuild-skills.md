# Command: /rebuild-skills
# Trigger: /rebuild-skills
# Reads: career-profile/profile.md, all projects/*.md, career-profile/skills.md (existing)
# Writes: career-profile/skills.md (on user confirmation)
# Requires: setup complete, at least one project page exists

**What it does:** Regenerates `skills.md` from all project pages
and `profile.md`. Presents the proposed new file and asks for confirmation before writing.

1. Read `profile.md` and all files in `projects/`
2. For each skill in the Core Competencies and Skills sections of `profile.md`:
   - Find all project pages that list this skill in Skills Demonstrated
   - Determine the highest evidence_level among those projects
   - Collect artifacts mentioned across those project pages
3. Build the new `skills.md`:
   - One section per skill
   - Evidence: list of [[wikilinks]] to project pages
   - Evidence Level: highest level found, with the source project noted
   - Artifacts: aggregated from project pages, deduplicated
   - Confidence: carry over from existing `skills.md` if present; otherwise leave blank for user
   - Gaps: leave blank for user to fill in
4. Show the proposed file to the user
5. Ask for confirmation before overwriting `skills.md`
6. On confirmation: write the file to `skills.md`.
   Report: skills updated, skills added, skills with no evidence found.
