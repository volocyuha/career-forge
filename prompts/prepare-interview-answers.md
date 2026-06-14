# Prompt: Prepare Interview Answers

Use this prompt to generate STAR stories for a specific role.
Run before an interview or application.

---

```
Read the following files from this repository:
- career-profile/profile.md
- career-profile/skills.md
- career-profile/target-role.md
- The 2-3 most relevant project pages for this role

Generate interview preparation for the role: [ROLE TITLE]

Produce three categories:

1. Competency questions (3-5 questions)
   For each: the question, a model STAR answer using only wiki evidence,
   and follow-up probes the interviewer is likely to ask

2. Behavioural questions (2-3 questions)
   For each: the question and a model STAR answer using wiki evidence

3. Weak spot questions (2-3 questions)
   Questions where my evidence is thin. For each: the question, what the gap is,
   and an honest prepared answer that doesn't undersell

Rules:
- All model answers must use only evidence present in the repository
- If a question has no good answer in the wiki, say so explicitly
- Do not invent experience or outcomes
- Weak spot answers must be honest — no fabrication, no overselling

Save output to: interview-prep/star-stories.md (append, do not overwrite)
```
