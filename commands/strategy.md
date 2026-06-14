# Command: /strategy
# Trigger: /strategy
# Reads: career-profile/profile.md, career-profile/current-role.md, career-profile/skills.md, career-profile/target-role.md, gap-analysis/*.md
# Writes: career-profile/strategy.md (on user confirmation)
# Requires: setup complete, gap analysis exists or /gap run first

**What it does:** Generates or updates `strategy.md` based on the
current state of all modules.

1. Read `profile.md`, `current-role.md`, `skills.md`, `target-role.md` and `gap-analysis/`
2. Identify the primary target role from `profile.md` (`gap_target` field)
   or ask the user if not set
3. Generate a strategy document with:
   - Current position summary (evidence-based, 2-3 sentences)
   - Target position and realistic timeline given current gaps
   - Strategic direction in plain language
   - Next best projects ordered by strategic impact, with scope and portfolio output defined
   - Career positioning statement for CV, LinkedIn, and cover letters
   - Application strategy: where to apply, in what order, and when
4. Rules:
   - Base all recommendations on actual evidence in the repository
   - Do not recommend applying before critical gaps are closed
   - Be direct — strategic clarity is more useful than encouragement
   - Mark any assumption as `[Assumption: needs confirmation]`
5. Present the proposed document and ask for confirmation before saving
6. On confirmation: save to `career-profile/strategy.md`
