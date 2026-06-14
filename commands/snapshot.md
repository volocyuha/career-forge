# Command: /snapshot
# Trigger: /snapshot
# Reads: career-profile/profile.md, all projects/*.md, outputs/
# Writes: nothing
# Requires: setup complete

**What it does:** Quick overview of current wiki state and one recommended next action.

1. Read `profile.md` and all files in `projects/`
2. Report:
   - Total project pages and publication status (from `visibility` frontmatter)
   - Projects with `[TBD]` markers
   - Projects with no outcome metrics
   - Projects missing from Skills section links in `profile.md`
   - Most recent output in `outputs/` (if any)
3. End with one recommended next action
