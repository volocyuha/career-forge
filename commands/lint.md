# Command: /lint
# Trigger: /lint
# Reads: career-profile/profile.md, all projects/*.md
# Writes: only files explicitly approved by the user
# Requires: setup complete

**What it does:** Read-only health check of the whole wiki.
No edits without explicit user approval.

1. Read `profile.md` and all files in `projects/`
2. Check for:
   - Wikilinks in `profile.md` that don't resolve to a file in `projects/`
   - Project pages with no inbound link from `profile.md`
   - `[TBD]` markers (list with their explanation)
   - Tags not present in the Skills section of `profile.md`
   - Missing required sections: Overview, My Responsibilities, Process, Outcome, Lessons Learned
   - Outcome sections with no concrete result
   - Lessons Learned sections that are generic rather than project-specific
   - `card_result` fields that describe the product rather than a professional outcome
3. Present findings by severity: Broken / Incomplete / Weak
4. Ask which items to fix and which the user will handle manually
5. Only edit files the user explicitly approves. Confirm each fix after writing.
