# Command: /profile-check
# Trigger: /profile-check
# Reads: career-profile/profile.md, career-profile/current-role.md, career-profile/skills.md
# Writes: nothing — read-only audit
# Requires: setup complete

**What it does:** Audits the career profile for completeness and internal consistency.

1. Read `profile.md`, `current-role.md`, `skills.md`
2. Check:
   - Are all `[PLACEHOLDER]` fields in `profile.md` filled in?
   - Are strengths in `current-role.md` backed by High/Medium evidence in `skills.md`?
   - Are weaknesses acknowledged that are required for the `gap_target` role?
   - Is the elevator pitch specific (design philosophy) or generic (job title)?
   - Is the positioning statement role-specific or could it apply to anyone?
   - Are career constraints filled in?
3. Report each check as PASS / FAIL / MISSING
4. End with: profile complete / needs work / missing critical information
