# Prompt: Generate Portfolio Case Study

Use this prompt to turn a project page into a portfolio-ready case study.
Run after filling in a project page thoroughly.

---

```
Read the following files:
- projects/[slug].md
- guidelines/*.md
- career-profile/profile.md (AI Context section)

Generate a portfolio case study for this project following the rules in portfolio-rules.md.

The case study must:
1. Frame around the designer's specific problem, not the game's description
2. Answer the four career evidence questions:
   - What problem did I solve?
   - Why did I choose this solution?
   - What was the result?
   - What proves it?
3. Include the process formula for each major design decision:
   - Result (stated first)
   - Problem
   - Diagnosis
   - Solution (with WHY this approach over alternatives)
   - Outcome
   - Retrospective
4. Include a Lessons Learned section specific to this project
5. Flag where visuals are missing and what type would be most useful

Rules:
- Never describe the game like a Steam page
- Every sentence must describe the designer's thinking, not the game's features
- No em dashes anywhere
- No negations (X isn't just Y / X is more than Y)
- Use only evidence from the project page — do not invent outcomes

Output format: markdown, ready to paste into the portfolio site or save to outputs/
```
