# Command: /interview [role]
# Trigger: /interview [role]  e.g. /interview technical-quest-designer
# Reads: career-profile/profile.md, career-profile/skills.md, career-profile/current-role.md, 2-3 project pages
# Writes: interview-prep/star-stories.md (on user confirmation)
# Requires: setup complete

**What it does:** Generates a mock interview session based on the wiki. The AI plays an
interviewer for the specified role type, draws questions from real project decisions and
outcomes, and identifies weak spots to prepare for.

**Example:** `/interview technical-quest-designer`

1. Read `profile.md`, `skills.md`, `current-role.md`,
   and the 2-3 most relevant project pages for this role
2. Generate three question categories:

   **Competency questions** — drawn directly from project decisions in the wiki
   For each: the question, a model answer grounded in wiki evidence, and follow-up probes
   the interviewer is likely to ask
   Example: "Walk me through a quest system you designed. How did you handle state tracking?"

   **Behavioural questions** — drawn from leadership, process, and challenge moments
   For each: the question, a model STAR-format answer using wiki evidence
   Example: "Tell me about a time a design decision didn't work and how you responded."

   **Weak spot questions** — questions the interviewer will ask where current wiki evidence
   is thin, missing, or only Low evidence level
   For each: the question, what the weakness is, and what to say honestly without underselling

3. End with a preparation summary:
   - Strongest talking points (High/High+ evidence skills)
   - Riskiest questions (Low evidence or missing skills for this role)
   - Suggested project to add that would close the biggest gap

The AI does not fabricate experience. All model answers use only wiki evidence.
If a question has no good answer in the wiki, it says so explicitly.

After generating, ask the user whether to save to `interview-prep/star-stories.md`.
