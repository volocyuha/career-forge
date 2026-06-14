# Command: /generate
# Trigger: /generate
# Reads: career-profile/profile.md, guidelines/*.md, 1-2 relevant project pages
# Writes: outputs/cv-[studio]-[YYYY-MM-DD].md, outputs/cover-[studio]-[YYYY-MM-DD].md
# Requires: setup complete

**What it does:** Produces a tailored CV and cover letter for a specific role.

Before starting, ask the user for:
- Job title and company name
- Job description (paste or URL — fetch if URL provided)
- Optionally: vacancy page URL for additional context

1. Read `profile.md` in full and all `.md` files in `guidelines/`
2. Identify role type from the Positioning Notes section of `profile.md`
3. Read the 1-2 most relevant project pages for this role
4. Write the CV:
   - Lead with most role-relevant experience, not chronological order
   - Every bullet: [action verb] + [specific deliverable] + [measurable result]
   - Use 3-4 bullets per role (minimum 2, maximum 5)
   - Cut content that doesn't serve this application
   - No em dashes, no passive voice, no "was responsible for", no negations
   - Never invent experience not in the wiki
   - One page where possible
5. Write the cover letter:
   - Open with a specific hook tied to this role or studio, never "I am writing to apply"
   - 3-4 paragraphs: hook, evidence from 1-2 projects, fit, call to action
   - Conversational but professional, no em dashes, no negations
6. Save to `outputs/cv-[studio]-[YYYY-MM-DD].md` and `outputs/cover-[studio]-[YYYY-MM-DD].md`
7. Report: which projects were used, positioning choices made
