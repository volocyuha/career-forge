# Prompt: Generate Gap Analysis

Use this prompt to generate or refresh your gap analysis.
Run after updating your evidence tracker or adding new projects.

---

```
Read the following files from this repository:
- career-profile/profile.md
- career-profile/current-role.md
- career-profile/target-role.md
- career-profile/skills.md
- All files in projects/

Compare my current evidence against the requirements of my target role.

Generate a gap analysis with four sections:

1. Already Strong — skills with High or High+ evidence relevant to the target role
2. Partial Evidence — skills present but at Medium or Low level
3. Missing or Weak Evidence — required skills with no evidence or only Low level
4. Recommended Portfolio Projects — 3-5 concrete projects that close the priority gaps,
   ordered by impact-to-effort ratio. For each: what to build, skills evidenced,
   realistic evidence level achievable, and scope estimate.

Do not invent skills or experience not in the repository.
Mark gaps clearly. Do not soften the analysis to be encouraging.

Save output to: gap-analysis/[target-role]-gap.md
```
