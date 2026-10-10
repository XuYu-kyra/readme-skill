---
name: job-portfolio-readme
description: Create or revise evidence-based bilingual README files for public GitHub projects used in job applications, recruiter review, portfolios, or technical interviews. Use when positioning real project work, clarifying personal contribution and attribution, improving Chinese/English naturalness, or separating internal audit findings from public-facing copy. Do not use for ordinary API references, contributor manuals, or security audit reports.
---

# Job Portfolio README

Create a public recruiting artifact grounded in repository evidence. Select and
sequence the strongest true facts; never invent results, capabilities, or
ownership.

## Load relevant guidance

- Read `references/quality-rubric.md` before drafting.
- Read `references/project-archetypes.md` to choose a project-specific
  structure. Treat it as a menu, not a template.
- Read `references/bilingual-style.md` when the README has Chinese and English
  editions.

## Separate public copy from the internal report

Keep two distinct outputs:

1. **Public README:** project value, personal role, technical depth, decisions,
   results, evidence or demo, setup, and concise attribution.
2. **Private delivery report:** security remediation, credential rotation,
   uncertain provenance, repository hygiene, missing production hardening,
   unverified facts, and suggested follow-up work.

Never paste the private report into the README. Mention a limitation publicly
only when omitting it would make a material claim misleading; state it neutrally
and briefly near the relevant claim.

Examples that belong in the private report:

- Current or historical exposed credentials and rotation advice.
- Missing lockfiles, queues, monitoring, rate limits, or other hardening ideas.
- Cleanup suggestions and repository hygiene observations.
- A claim whose provenance is uncertain. Omit that claim until confirmed.

Examples that may belong in the public README:

- Concise ownership attribution for upstream or team work.
- Experimental scope needed to interpret a measured result.
- Real prerequisites required to run the project.
- A short, accurate description such as “research prototype.”

## Workflow

### 1. Resolve audience and scope

Determine the target role, language order, whether the user wants review,
drafting, or direct edits, desired depth, and available media. If unspecified,
optimize for a recruiter plus a technical interviewer: professional, detailed
enough for follow-up questions, and easy to scan. Prefer verified media over
badge walls.

### 2. Inspect evidence

Inspect the current README, repository tree, entry points, dependency manifests,
tests, architecture documents, result artifacts, demos, license files, and
attribution notices. Treat the old README as a claim source, not final authority.

Maintain a private evidence ledger:

`claim -> repository evidence -> confidence -> ownership -> public / internal / omit`

Do not publish this ledger unless the user asks for it. Never expose secret
values in any output.

### 3. Identify the portfolio thesis

Write one sentence combining:

- the problem or user outcome;
- the candidate's real responsibility;
- the strongest verified result, capability, or engineering decision.

Use that thesis to choose what belongs above the fold. Never add headings such
as “Why this matters to recruiters” or “Why this is useful in an interview.”

### 4. Choose a project archetype

Select the closest archetype from `references/project-archetypes.md`, then
adapt it to the repository. Do not force unrelated projects into identical
headings or section order.

Design three reading depths:

- **15 seconds:** title, one-line value, strongest visual or result, role.
- **2 minutes:** architecture, contribution, tech stack with actual roles,
  evidence.
- **Interview depth:** decisions, trade-offs, evaluation, reproducibility, and
  attribution.

### 5. Draft the public README

- Use concrete verbs and specific nouns.
- Put a strong verified result, workflow, or demo near the top.
- Explain technologies through what they do in this project.
- Distinguish **authored**, **adapted**, **integrated**, **extended**, and
  **team-owned** work.
- Express engineering thinking as
  `constraint -> decision -> consequence`, not as self-praise.
- Include commands only when they match the repository.
- Keep attribution visible and concise.
- Omit speculative roadmaps and generic “future work” filler.

### 6. Write bilingual editions

Build both languages from the same verified fact model. Preserve the same
important claims, numbers, links, evidence, and ownership boundaries, but write
each language naturally rather than translating sentence by sentence. The
Chinese edition must not be a compressed summary of the English edition.

### 7. Review before editing

Score the draft with `references/quality-rubric.md`. Also apply this recruiter
test:

- Is the project's value clear on the first screen?
- Is the candidate's personal contribution unambiguous?
- Is there at least one concrete result, artifact, or demo?
- Did any internal audit note leak into the public copy?
- Does the structure sound specific to this project?

### 8. Deliver separately

Change only files authorized by the user. In the final delivery, report:

- changed file paths;
- the positioning and structural changes;
- evidence checked;
- checks performed;
- unknowns or attribution questions that still need confirmation.

Keep security findings and private defects outside the README.

## Non-negotiables

- Never fabricate measurements, deployment status, user adoption, training, or
  ownership.
- Never weaken upstream or collaborator attribution for stronger marketing.
- Never put credentials or credential-remediation instructions in public copy.
- Never turn a portfolio README into an audit report, backlog, or apology.
- Never reuse one rigid template across distinct project types.
- Never make one language materially thinner than the other.
- Never mutate files when the user requested review or a draft only.
