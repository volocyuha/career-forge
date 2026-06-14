# Command: /link-skills [slug]
# Trigger: /link-skills [slug]  e.g. /link-skills project-name
# Reads: projects/[slug].md, career-profile/profile.md, career-profile/skills.md
# Writes: career-profile/profile.md, career-profile/skills.md (on user confirmation)
# Requires: setup complete

**What it does:** Syncs a project's Skills Demonstrated section into `profile.md` and
triggers a `skills.md` update for affected skills. Confirms all changes before writing.

1. Read Skills Demonstrated in `projects/[slug].md`
2. Read Core Competencies and Skills sections in `profile.md`
3. Read `skills.md`
4. Compile changes: links to add in `profile.md`, skill entries to update in `skills.md`
5. Show the full list and ask for confirmation
6. On confirmation: apply changes to both files
7. Report: links added, skills updated, tags added
