# Command: /ats [optional: slug or filename]
# Trigger: /ats  or  /ats cv-studio-2024-11-01
# Reads: job description (pasted or fetched), career-profile/profile.md or specified output file
# Writes: nothing — analysis only
# Requires: setup complete

**What it does:** Analyzes a vacancy against the wiki or a specific CV for ATS keyword
gaps and formatting issues. If a CV file is provided, analyzes that; otherwise reads `profile.md`.

**Example:** `/ats` (analyzes profile against pasted JD)
**Example:** `/ats cv-studio-2024-11-01` (analyzes a specific output file)

Before starting, ask for the job description (paste or URL — fetch if URL provided).

1. Read the job description
2. Read the target document (`profile.md` or the specified file)
3. Run two analyses:

   **Keyword analysis**
   - Extract hard skills, tools, and discipline terms from the JD
   - Check each against the target document
   - Report as: PRESENT / MISSING / PARTIAL (mentioned but not prominent)
   - Flag the top 5 missing or underweighted keywords most likely to matter for ATS scoring

   **Formatting analysis** (if analyzing a CV output file)
   - Flag: tables (often ATS-broken), columns (often parsed incorrectly), special characters,
     headers that don't match standard ATS field names, missing sections (summary, skills list)
   - Report each issue with a specific fix

4. End with a priority fix list: the 3 changes most likely to improve ATS pass rate
   Do not rewrite the CV — list the specific changes for the user to apply
