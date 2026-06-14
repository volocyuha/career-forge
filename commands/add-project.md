# Command: /add-project
# Trigger: /add-project
# Reads: new-project.md, guidelines/*.md
# Writes: projects/[slug].md, career-profile/profile.md, new-project.md (reset)
# Requires: setup complete, new-project.md filled in

**What it does:** Reads `new-project.md`, checks framing, creates a project page,
integrates it into the wiki, resets the intake form.

1. Read all `.md` files in `guidelines/` and `new-project.md`
2. Check framing using signals from the Detecting Misleading Framing section of the guidelines.
   If framed around the product rather than the professional's decisions — stop, do not create the page yet:
   - List exactly which signals were triggered
   - Give a before/after recommendation for each problem
   - Report each item as OK or NEEDS WORK:
     - [ ] Frames around a specific design problem, not the game's description
     - [ ] States what the user personally owned (not "we")
     - [ ] Answers why this approach over alternatives
     - [ ] Has at least one concrete outcome or observable change
     - [ ] Responsibilities show decision authority, not just task completion
   - Ask the user to update `new-project.md` and run `/add-project` again. Stop here.
3. Ask: which category (Work Experience / Side Project / Other) and where to place it
   within that category. Wait for the answer before continuing.
4. Create `projects/[slug].md` from `projects/_PROJECT_TEMPLATE.md`
   Fill all sections from the notes. Mark gaps as `[TBD: what's needed and why]`
5. Add the project to the correct section of `profile.md` at the specified position
6. Add `-> [[slug]]` links to matching skill entries in Core Competencies in `profile.md`
7. Verify tags exist in the Skills section of `profile.md`; add any new ones
8. Reset `new-project.md` to its blank template state
9. Report: what was created, all `[TBD]` items and what's needed, which skills were linked
