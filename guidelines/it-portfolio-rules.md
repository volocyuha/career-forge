# IT Portfolio Guidelines

# Purpose: Writing and reviewing portfolio case studies for general IT roles.
# Applies to: /add-project, /import-project, /review, /generate, /cleanup-setup
# Field: General IT (software engineering, product design, DevOps, data, PM, UX)
# Note: Use alongside portfolio-rules.md, or replace it if not working in gamedev.

These are operative rules the AI must apply when writing, reviewing, or improving
project pages and portfolio content for IT professionals. Not a summary for reading
— a ruleset for generating.

---

## The Foundational Rule

A portfolio is not a list of technologies used. It is a showcase of how a professional
thinks, solves problems, and delivers value. Every sentence written must answer the
hiring manager's real question: what will this person do on my team?

**Test every sentence:** does it describe the system, or does it describe the professional's
thinking and decisions? If it describes the system, rewrite or cut it.

---

## Detecting Misleading Framing

Check every project description before writing. Flag and stop if the input is
technology-framed rather than impact-framed.

### Signals that a description is tech-framed, not impact-framed

- Leads with a tech stack list rather than a specific problem to solve
- Uses "we" throughout with no clear individual ownership
- Describes features built ("the app had a REST API") rather than decisions made
  ("I designed the API contract to decouple frontend release cycles from backend")
- No answer to why a specific approach was chosen over alternatives
- Outcome describes the system ("the app was deployed") not the impact
  ("deployment time dropped from 45 minutes to 4 minutes")
- Role described vaguely ("I worked on the backend") with no scope or deliverable

### How to flag it

Stop before writing. Tell the user exactly which signals were triggered.
Give a before/after example for each problem. Run the framing checklist:

- [ ] Frames around a specific technical or business problem
- [ ] States what the user personally owned and decided
- [ ] Answers why this approach over alternatives
- [ ] Has at least one concrete outcome with measurable impact
- [ ] Responsibilities show decision authority, not just task completion

Ask the user to update their notes and re-run. Stop here until framing is corrected.

---

## The Three Questions

Every project page and CV bullet must satisfy all three:

1. What was the problem? (specific, not "I built a feature")
2. Why this solution and not another? (reasoning must be explicit)
3. What was the outcome? (measured or observed — numbers strongly preferred)

---

## Rules for Writing Project Pages

### Framing
- Never describe a project like a GitHub README (tech stack, features, setup instructions)
- Always frame around the professional's specific problem and ownership
- Lead the Overview with the business or technical problem, not the solution
- End the Overview with the core constraint or trade-off that shaped the approach

Wrong: "Built a microservices architecture using Node.js, Docker, and Kubernetes."
Right: "The monolith was blocking three teams from deploying independently.
I designed the service boundary strategy to decouple release cycles
without requiring a full rewrite."

### The Process Formula
Apply to each significant technical decision:

```
Result     — state the outcome first, one sentence
Problem    — what specific challenge or constraint
Diagnosis  — how the root cause was identified (profiling, user research, metrics)
Solution   — what was done and WHY THIS APPROACH over alternatives
Outcome    — what changed, measured or observed
Retrospective — what would be done differently
```

### Responsibilities
Each responsibility: [action verb] + [specific deliverable] + [scope or scale]

Wrong: "Responsible for backend development."
Right: "Designed and implemented the authentication service handling 2M daily active users,
reducing login latency from 800ms to 120ms."

### Outcomes
Strong: quantitative metric with before/after (latency, error rate, cost, time, NPS)
Strong: shipped to real users with adoption data
Medium: internal tool adopted by the team
Medium: open source project with stars/forks/contributors
Weak but honest: prototype validated with user testing

### Lessons Learned
- Specific to this project, not generic
- Not blaming tools, teams, or circumstances
- End with "What I'd do differently:" followed by a concrete action

---

## Rules for Writing CVs

- Lead with most role-relevant experience, not chronological order
- Every bullet: [action verb] + [specific deliverable] + [measurable result]
- No passive voice. No "was responsible for." No "helped with."
- No em dashes, no negations
- One page for under 7 years experience; two pages maximum after that
- Skills section: list tools and technologies plainly, no proficiency bars

---

## Rules for Writing Cover Letters

- Open with a specific hook tied to the role or company problem — never "I am writing to apply"
- 3-4 paragraphs: hook, evidence from 1-2 projects, fit, call to action
- Conversational but professional
- Connect specific technical decisions to the role's known challenges
- No em dashes, no negations

---

## Rules for Reviewing Content

Report each item as PASS / FAIL / NEEDS INPUT:

- [ ] Frames around a specific technical or business problem
- [ ] Overview states what the user owned and what constraint shaped the approach
- [ ] Every responsibility: action verb + deliverable + scope
- [ ] Each major decision follows the process formula with explicit WHY
- [ ] At least one quantified outcome
- [ ] Lessons Learned is project-specific, not generic
- [ ] `card_result` states impact, not technology used
- [ ] No em dashes, no negations
- [ ] Responsibilities separate individual work from team work

---

## What the AI Should Never Do

- List technologies as the primary content of a project page
- Use "passionate about" or "love working with" anywhere
- Write outcomes that describe the system ("was deployed", "was built")
  instead of the impact ("reduced costs by 40%", "cut deployment time from 45min to 4min")
- Invent metrics, adoption numbers, or business outcomes not in the wiki
- Use em dashes or negations anywhere in generated output
