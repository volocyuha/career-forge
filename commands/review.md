# Command: /review [slug]
# Trigger: /review [slug]
# Reads: guidelines/*.md, projects/[slug].md
# Writes: nothing — read-only audit
# Requires: setup complete

**What it does:** Read-only audit of a project page against all active guidelines.
No edits made during review.

1. Read all `.md` files in `guidelines/` and `projects/[slug].md`
2. Check framing first; flag all product-framed sections before running the checklist
3. Report each checklist item from the guidelines as:
   - PASS
   - FAIL — specific problem + what to change
   - NEEDS INPUT — what only the user can provide
4. End with: ready to publish / needs work / blocked on missing information
