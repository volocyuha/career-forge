# Command: /cleanup-setup
# Trigger: Automatically after /setup completes all modules. Can also be run manually.
# Reads: commands/setup.md Setup Status table
# Writes: career-profile/profile.md, career-profile/current-role.md, career-profile/target-role.md, career-profile/skills.md, commands/setup.md
# Requires: setup complete — check Status table first

**What it does:** Strips setup scaffolding from filled files, leaving only real content.
Reduces noise in AI context on every subsequent session.

**Never run this if setup is incomplete** — check the Setup Status table in `commands/setup.md` first.
If any module shows Pending, ask the user whether to skip that module or complete it first.

1. Read `commands/setup.md` Setup Status table. If any module is still Pending, stop and ask.
2. Clean each file in this order, showing a before/after diff and asking for confirmation
   before writing:

   **`profile.md`**
   - Remove any line that still contains `[YOUR` placeholder text
   - Remove inline instruction comments (lines starting with `>` that are instructions,
     not real content — distinguish by checking if the line contains words like
     "replace", "example", "e.g.", "fill in", "your", "placeholder")
   - Keep all real data, wikilinks, section headers, and the Claude Context section
   - Keep any `[TBD:` markers — those are intentional gaps, not scaffolding

   **`career-profile/current-role.md`**
   - Remove lines that are purely instructions in brackets: lines like
     `[Your summary here]`, `[Your reasoning here]`, `[Add your specific assets here]`
   - Remove checklist items the user has not filled (empty `- [ ]` items with no content)
   - Keep all real answers, filled checkboxes, and section headers

   **`career-profile/target-role.md`**
   - Remove instruction lines in brackets that were not replaced with real content
   - Remove `[Your reasoning here]` and equivalent unfilled placeholder lines
   - Keep all real content, section headers, and any `[TBD:` markers

   **`career-profile/skills.md`**
   - Remove the Evidence Level Scale table — it lives in `commands/setup.md` and `WIKI_GUIDE.md`,
     no need to carry it in the skills file after setup
   - Keep all skill entries and the summary table

   **`commands/setup.md`**
   - Remove the entire "AI Instructions for Setup" section
   - Remove the entire "Setup Checklist" section
   - Remove the "What Setup Does Not Do" section
   - Keep only: the file header, the Setup Status table (as a permanent record),
     and a one-line note: "Setup completed. See WIKI_GUIDE.md for ongoing system usage."

3. After all files are cleaned, confirm: "Setup scaffolding removed. Your knowledge base
   is clean. Run /snapshot to see the current state."

What cleanup must never remove:
- Real content provided by the user
- `[TBD:` markers — these are intentional gaps flagged for follow-up
- Section headers
- The Setup Status table in `commands/setup.md`
- Wikilinks (`[[slug]]` format)
- The Claude Context section in `profile.md`
- `#>` instruction comments in `_PROJECT_TEMPLATE.md` — not touched by cleanup
