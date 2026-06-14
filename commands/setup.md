# Setup Guide — Career Forge

This file serves two purposes:
1. Instructions for the AI on how to conduct initial setup
2. A record of what was completed during your setup session

After setup is complete, the AI will mark each section below as DONE or SKIPPED.

---

## Setup Status

> Updated by the AI after each setup session.

| Module | Status | Method | Date |
|---|---|---|---|
| `career-profile/profile.md` | Pending | — | — |
| `career-profile/current-role.md` | Pending | — | — |
| `career-profile/target-role.md` | Pending | — | — |
| `career-profile/skills.md` | Pending | — | — |
| First project page | Pending | — | — |

---

## AI Instructions for Setup

Read this section before starting setup with a new user.

### First-Run Detection

Before running any other command, check whether `career-profile/profile.md` contains
`[YOUR NAME]` or any other `[PLACEHOLDER]` text. If it does, the repository has not been set up.

Greet the user:

"Welcome to Career Forge. Before we can generate CVs, run gap analysis,
or prepare for interviews, I need to build your knowledge base.

You have two options:

**Option A — Share your CV and portfolio**
Paste your CV as text, share a link to your portfolio, or upload a file.
I'll extract your information and fill in the system automatically.
You'll review and confirm everything before it's saved.

**Option B — Answer a few questions**
I'll walk you through a short interview (around 15-20 minutes).
No CV needed. Your answers become the foundation of your knowledge base.

Which would you prefer?"

Wait for the user's answer before continuing.

---

### Option A: CV and Portfolio Extraction

1. Ask the user to paste their CV as text, or provide a portfolio URL to fetch
2. If a URL is provided, fetch the page before proceeding
3. Extract the following from the provided material:

   From CV:
   - Full name, contact details, location
   - Current job title
   - Work history (title, studio, project, dates, bullet points)
   - Education
   - Languages
   - Listed skills and tools

   From portfolio (if provided):
   - Project names and descriptions
   - Role descriptions
   - Any outcomes or metrics mentioned
   - Tools and disciplines demonstrated

4. Show the user a structured summary of what was extracted:
   "Here's what I found. Review this before I build your files:"
   [display structured summary]
   "Is anything missing, incorrect, or sensitive that you'd like to remove?"

5. Wait for confirmation or corrections

6. Fill in the files listed in the Setup Checklist below, in order
7. For anything not found in the CV or portfolio, mark as `[TBD: not in CV — add manually]`
8. After filling each file, show a summary of what was written and ask for confirmation
   before moving to the next file
9. Update the Setup Status table in this file after each module is completed

---

### Option B: Guided Interview

Conduct the interview in sections. Ask one section at a time.
Do not ask all questions at once. Wait for answers before continuing.

After each section, summarize what you heard and confirm before moving on.

---

#### Section 1: Who You Are (5 minutes)

Ask these questions conversationally, not as a list:

1. What's your name, and what's your current job title or how do you describe yourself professionally?
2. Where are you based, and are you open to relocation or remote work?
3. How many years have you been working in your field — professionally, freelance, or in serious personal projects?
4. What types of projects have you worked on?

After answers: summarize and confirm.

---

#### Section 2: Your Experience (10 minutes)

5. Walk me through your most significant professional role. What studio or company, what project, what were you responsible for?
6. What's the work you're most proud of — shipped or not? What did you personally own in that project?
7. Have you worked on any other notable projects — freelance, personal, community, or cancelled? Tell me about them briefly.
8. Do you have a portfolio site or any public work I can reference? If yes, share the link.

After answers: summarize and confirm.

---

#### Section 3: Skills and Evidence (5 minutes)

9. What are your strongest skills — the ones you have real evidence for, not just familiarity?
10. What tools and engines have you worked with professionally? Which ones are you just familiar with?
11. What skills do you feel are weak or missing that you'd like to develop?

After answers: summarize and confirm.

---

#### Section 4: Career Direction (5 minutes)

12. What role are you targeting next? Be specific if you can — job title, not just "something in games" or "something in tech."
13. Why that role? What draws you toward it?
14. What's your timeline — are you actively applying now, or planning ahead?
15. Are there any constraints I should know about — location, visa, salary needs, availability?

After answers: summarize and confirm.

---

#### Section 5: Quick Facts (2 minutes)

16. What's your email and LinkedIn URL for the profile?
17. What languages do you speak and at what level?
18. Any education worth noting — especially if it's relevant to your work in a non-obvious way?

After answers: summarize and confirm.

---

### After the Interview

1. Show the user a complete summary of everything captured
2. Ask: "Anything to add, change, or remove before I build your files?"
3. Wait for final confirmation
4. Fill in the files listed in the Setup Checklist, in order
5. For anything not answered, mark as `[TBD: not provided — add manually]`
6. After filling each file, show a summary and ask for confirmation before the next
7. Update the Setup Status table in this file after each module is completed

---

## Setup Checklist

Fill these files in this order. Each depends on the previous.

### 1. `career-profile/profile.md`

Fill from: name, contact, title, target roles, elevator pitch, work history, education, languages, skills, quantified achievements.

Key fields that must not stay as placeholders:
- Name, email, location
- Current title and target roles
- `gap_target` field (the single role being worked toward)
- At least one work history entry
- Elevator pitch (specific, not generic)

### 2. `career-profile/current-role.md`

Fill from: experience summary, strengths with evidence, weaknesses, career assets, constraints.

Key fields:
- Strengths must reference actual projects, not just skill names
- Weaknesses must be honest — this drives gap analysis accuracy
- Constraints must be realistic (location, timeline, financial needs)

### 3. `career-profile/target-role.md`

Fill from: target role answer, required skills research, target companies if mentioned.

- Required skills: if the user doesn't know them, derive from common job postings
  and note: `[Derived from common JDs — confirm against real postings]`

### 4. First project page in `projects/`

Fill from: the most significant project mentioned in the interview or CV.

- Use `projects/_PROJECT_TEMPLATE.md` as the format
- Prioritize the project with the strongest evidence
- Mark gaps as `[TBD: what's needed]`
- After creating, run the framing check using all files in `guidelines/`

### 5. `career-profile/skills.md`

Fill from: extracted skills + the first project page.

- Only list skills with at least one project as evidence
- Set evidence_level accurately — do not inflate
- Leave Confidence and Gaps blank for the user to fill manually

### 6. Update Setup Status table

Mark each completed module as DONE with method (CV extraction / Interview) and date.

---

## What Setup Does Not Do

- Setup does not generate a CV or cover letter — that's `/generate`
- Setup does not run gap analysis — that's `/gap`
- Setup does not create all project pages — only the first one
- Setup does not fill in `career-profile/strategy.md` — run `/strategy` after setup

---

## After Setup Completes

When all modules in the Setup Checklist are marked DONE, the AI will automatically run
`/cleanup-setup`. This strips setup scaffolding from all filled files:

| File | What gets removed |
|---|---|
| `career-profile/profile.md` | Unfilled placeholders, inline instructions |
| `career-profile/current-role.md` | Instruction lines in brackets, empty checklist items |
| `career-profile/target-role.md` | Unfilled instruction lines |
| `career-profile/skills.md` | The Evidence Level Scale table (kept in WIKI_GUIDE.md) |
| `commands/setup.md` | AI Instructions, Setup Checklist, and What Setup Does Not Do sections |

What is never removed: real content, `[TBD:]` markers, section headers, wikilinks,
the Setup Status table, and the AI Context section in `career-profile/profile.md`.

After cleanup, this file will contain only the Setup Status table as a permanent record.
Run `/snapshot` to see what to do next.
