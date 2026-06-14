# Prompt: Create Evidence Map

Use this prompt to regenerate the evidence tracker from project pages.
Run after adding or updating project case studies.

---

```
Read the following files from this repository:
- profile.md
- All files in projects/

For each skill listed in the Core Competencies and Skills sections of profile.md:

1. Find all project pages that list this skill in their Skills Demonstrated section
2. Determine the highest evidence_level among those projects using this scale:
   - High: shipped in a team context, professional project
   - High+: High, plus metrics, revenue data, or significant player base
   - Medium: solo published, or team project not publicly shipped
   - Medium+: Medium, plus public playtests or publicly awarded jam work
   - Low: game jam, case study, experiment, cancelled, or in development
3. Collect concrete artifacts mentioned across those project pages

Generate an updated career-profile/skills.md with:
- One section per skill
- Evidence: wikilinks to project pages
- Evidence strength: highest level found, with source project noted
- Proof: specific artifacts and deliverables from project pages
- Confidence: leave blank if not in existing file
- Gaps: leave blank for user to fill in

Present the proposed file and ask for confirmation before saving.
```
