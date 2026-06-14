# Gamedev Portfolio Guidelines

# Purpose: Writing and reviewing portfolio case studies and project pages.
# Applies to: /add-project, /import-project, /review, /generate, /cleanup-setup
# Field: Game development (source: https://gamedev.work/guidelines/ Parts 1, 2, 3)
# To override or extend: add a new .md file to guidelines/ with a matching Purpose line.

These are operative rules the AI must apply when writing, reviewing, or improving
project pages and portfolio content. Not a summary for reading — a ruleset for generating.

---

## The Foundational Rule

A portfolio is not a showcase of games. It is a showcase of how a designer thinks,
solves problems, and makes decisions. Every sentence Claude writes must answer the
recruiter's real question: what will this person do on my team?

**Test every sentence:** does it describe the game, or does it describe the user's
thinking and decisions? If it describes the game, rewrite or cut it.

---

## Detecting Misleading Framing

When a user describes a project — in raw notes, a rough brief, or any input — Claude must
check the description against the foundational rule before writing anything.

If the input is framed around the game rather than the designer's decisions, Claude must
flag it explicitly before proceeding. Do not silently reframe it. Make the problem visible
so the user understands what needs to change in how they think and talk about their work.

### Signals that a description is game-framed, not designer-framed

- Leads with genre, platform, or team size rather than a specific design problem
- Uses "we" throughout with no clear statement of individual ownership
- Describes features ("the game had a branching quest system") rather than decisions ("I designed the branching quest system to solve X")
- No answer to why a specific approach was chosen over alternatives
- Outcome is described in terms of the game ("the game was well-received") rather than the work ("optional quest completion rose from 24% to 71%")
- Role is described vaguely ("I was involved in quest design") with no scope or deliverable

### How to flag it

Stop before writing the project page. Tell the user specifically what is missing, using
the three questions as the frame. Be direct — soft-pedalling this costs them interview opportunities.

Example flag:

"Before I write this up, I need to flag that the description you've given is framed around
the game rather than your decisions. I can see what the game did, but not what problem you
were specifically handed, why you made the choices you made, or what changed as a result of
your work. Can you answer these three things:

1. What was the specific design challenge you were responsible for solving?
2. Why did you approach it the way you did, and what alternatives did you consider?
3. What concretely changed or improved as a result of your work?

Once I have those, I can write a case study that actually shows how you think."

### When to proceed without flagging

If the input clearly answers at least two of the three questions with some specificity,
proceed and flag only the missing piece inline. Reserve the full flag for descriptions
that are almost entirely game-framed with no designer perspective present.

---

## The Three Questions

Every project page and every CV bullet must satisfy all three:

1. What was the problem? (specific, not generic — what design challenge was handed to them)
2. Why this solution and not another? (the most important question — reasoning must be explicit)
3. What was the outcome? (measured or observed — numbers preferred, qualitative acceptable)

If any of the three is missing, the content is incomplete. Flag it and ask for the missing piece
rather than inventing it.

---

## Rules for Writing Project Pages

### Framing
- Never describe the game like a Steam page (genre, features, screenshots list)
- Always frame around the user's specific design challenge and ownership
- Lead the Overview with what they owned and what constraint they was working within
- End the Overview with their core design question — the thing they kept returning to

Wrong: "[Game Name] is a mobile MMO RPG with a story mode."
Right: "My challenge was writing emotionally resonant narrative inside a session-based mobile game,
using a custom scripting system, while hitting monetization targets without compromising the story."

### The Process Formula
Apply this structure to each significant design decision, not once per project:

```
Result     — state the outcome first, one sentence
Problem    — what specific challenge or constraint
Diagnosis  — how the root cause was identified (data, playtests, research)
Solution   — what was done and WHY THIS APPROACH over alternatives
Outcome    — what changed, measured or observed
Retrospective — what would be done differently
```

The WHY is non-negotiable. "I did X" is a task log. "I did X because it solved Y for Z type of
player, and not A because A only addresses the symptom" is design thinking.

### Responsibilities
Each responsibility must follow: [action verb] + [specific deliverable] + [scope or scale]

Wrong: "Responsible for narrative and dialogue across the project."
Right: "Wrote ~35,000 words of in-game dialogue across 3 of 7 chapters, including the final act,
all within the framework I designed."

Separate what the user did from what the team did. Never write "we" for their individual decisions.

### Showing Iteration
Iteration is more valuable content than a polished final solution. When multiple versions exist,
structure them as named iterations (Version 1, Alpha Build, Post-playtest revision) with:
- What was tried
- Why it failed (specific evidence, not just "it didn't work")
- What changed between versions and why
- The final result

A failed first attempt followed by a successful revision is more impressive than only showing
the final solution.

### Visuals
Claude cannot generate images, but should flag where visuals are missing and what type would
help most. Priority order:
1. Flowcharts and diagrams (quest flow, state machines, dialogue trees)
2. Before/after comparisons showing design evolution
3. Process sketches (raw is fine — authentic process is valuable)
4. Design document excerpts
5. GIFs or short video
6. In-engine screenshots (Blueprint graphs, level editor, scripting tools)
7. Data visualizations

Visuals must be interspersed with the text they support, not collected at the bottom.
Every image needs a caption. A screenshot without a caption is decoration; with a caption, evidence.

When no visuals exist, suggest: "Recreate the diagram from memory and label it 'reconstructed
for portfolio'. A reconstructed flowchart is better than no flowchart."

### Outcomes
Numbers build credibility. Even rough or relative ones. Required in every project page.

Strong evidence: quantitative metric with before/after
Strong evidence: shipped with audience (review count, rating, sentiment)
Medium evidence: qualitative with source ("selected as best jam entry by jury of 5")
Medium evidence: milestone reached ("shipped on schedule with team of 8, no crunch")
Weak but honest: prototype validated ("playtested with 12 players, core loop felt readable")

When no hard numbers are available, use qualitative outcomes with a source:
"Post-launch reviews consistently cited the optional quest system as a highlight.
40+ Steam reviews mentioned specific quest names — a signal of meaningful engagement."

Internal adoption counts: "The Quest Design Bible was adopted as studio-wide standard."

### Lessons Learned
Required on every project page. Missing in most junior portfolios — that makes it a differentiator.

Rules:
- Must be specific to this project, not generic ("communication is important" is not a lesson)
- Must not blame the team, client, or circumstances — keep it about their own decisions
- Must frame as growth, not incompetence
- Must end with "What I'd do differently:" followed by a concrete, specific action

Wrong: "I learned the importance of planning ahead."
Right: "I'd establish flag architecture in pre-production, not mid-production.
We lost 6 weeks retrofitting early quests that were designed before the system was stable."

---

## Rules for Writing CVs

### Positioning
- Lead with the most role-relevant experience, not chronological order
- Use Positioning Notes in profile.md to determine emphasis for each role type
- Cut content that doesn't serve the specific application — completeness is not the goal
- One page where possible

### Bullets
- Every bullet must follow: [action verb] + [specific deliverable] + [measurable result]
- No passive voice. No "was responsible for." No "helped with."
- No em dashes anywhere in output

### What not to invent
Never fabricate experience, metrics, or skills not present in profile.md or project pages.
If a claim can't be evidenced by the wiki, it does not go in the CV.

---

## Rules for Writing Cover Letters

- Open with a specific hook tied to the role or studio — never "I am writing to apply"
- 3-4 paragraphs: hook, evidence (1-2 specific projects), fit, call to action
- Conversational but professional — write like a confident colleague, not a LinkedIn profile
- Connect the user's concrete decisions to the role's specific needs
- End with a clear, direct call to action
- No em dashes

---

## Rules for Writing Copy (Card Results, Elevator Pitches, About Text)

### Card results (one-liner per project)
State a result, not a feature. Think: headline of a news article about the work.

Wrong: "I was the game designer on a fantasy RPG with a quest system."
Right: "Architected a 60-quest reactive system where Act 1 choices visibly reshape the world in Act 3."

### Elevator pitch
1-2 sentences. Design philosophy or specific value — not a job title.

Wrong: "I'm a passionate game designer with experience in multiple disciplines."
Right: "I design quests that make players care. Reactive systems where early choices reshape
the world — and documentation that keeps teams aligned when the system grows complex."

### Writing style rules (apply to all output)
- Sentences under 25 words where possible
- Active voice, subject first
- Cut adverbs and qualifiers (somewhat, fairly, quite, very)
- If an adjective isn't doing real work, remove it
- Each paragraph makes one point — if it runs past 5 sentences, split it
- Reading level: an intelligent person outside games should be able to follow it
- Write like a confident colleague explaining their work, not a formal document or hype piece
- No skill bars or percentage proficiency claims — let projects prove skills
- No em dashes or negations anywhere

---

## Rules for Reviewing Content

When asked to review a project page, check against this list and report pass/fail/needs-input
for each item:

- [ ] Page frames around the user's design problem, not the game's description
- [ ] Overview states what they owned and what constraint they was working within
- [ ] Every responsibility uses action verb + specific deliverable + scope
- [ ] Each major decision follows the process formula (problem, diagnosis, solution with WHY, outcome)
- [ ] At least one diagram or visual is present (or flagged as missing with a recommendation)
- [ ] Visuals are interspersed, not bottom-loaded
- [ ] At least one iteration is shown (before/after, version comparison, or playtest-driven change)
- [ ] Outcomes section has specific numbers or clearly evidenced qualitative results
- [ ] Lessons Learned is present and specific to this project
- [ ] card_result is a result statement, not a feature description
- [ ] tags use exact names from the Skills section of profile.md
- [ ] No em dashes in the text
- [ ] Responsibilities separate what they did from what the team did

---

## What Claude Should Never Do

- Write "I am passionate about games" or any equivalent generic opener
- List skills with percentage bars or proficiency levels — skills are proven by projects
- Use "we" for decisions the user made individually
- Invent outcomes, metrics, or experience not in the wiki
- Write lessons learned that apply to any project ("planning is important")
- Describe a game's genre and features as the primary content of a project page
- Use em dashes anywhere in generated output
- Add a new project page or skill link without evidence in the wiki to support it
- Present a process section as a version history without explaining WHY things changed

---

## Maintenance Rules

Add a new project to the portfolio only when all four criteria are met:
1. Can answer all three questions (problem, why this solution, outcome)
2. Has at least one concrete outcome to state
3. Has had time for reflection (a case study written 3 months post-ship is better than one written the week it launches)
4. The work can be separated clearly from the team's contribution

Set a quarterly reminder to review: availability status, job title, featured project relevance,
resume PDF date, all contact and social links, page load speed, any WIP projects resolved.

An outdated portfolio is worse than no portfolio. It signals nothing worth showing in over a year,
even if the work exists.
