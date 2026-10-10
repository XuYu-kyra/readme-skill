# Quality Rubric

Use this rubric before delivering a recruiter-facing README. Target at least
80/100 without triggering an automatic failure.

| Area | Points | What good looks like |
|---|---:|---|
| First-screen clarity | 15 | The reader quickly understands the project, value, and candidate role. |
| Problem and value | 10 | The real problem and intended user or research value are concrete. |
| Personal contribution | 20 | Authored, adapted, integrated, extended, and team work are separated. |
| Technical depth | 15 | The stack is explicit and each major technology has a real role. |
| Engineering judgment | 10 | At least one meaningful constraint, decision, and consequence is shown. |
| Results and evidence | 15 | Claims point to measurements, demos, artifacts, screenshots, or code. |
| Recruiter readability | 5 | Strong information appears early and sections are easy to scan. |
| Bilingual quality | 5 | Both editions are natural and materially complete. |
| Reproduction and navigation | 5 | Valid setup, usage, documentation, and source links are easy to find. |

## Automatic failures

- Ownership conflicts with source headers, attribution, or repository history.
- Results, deployment, training, or user outcomes are unsupported.
- A credential or secret value appears in the README.
- An upstream model or system is presented as original work.
- One language edition omits major contribution, evidence, or attribution.

## Public-content decisions

| Finding | Public README treatment |
|---|---|
| Strong verified result | Put near the top with scope and evidence. |
| Useful screenshot or demo | Put early; caption what the reader should notice. |
| Meaningful trade-off | Explain constraint, decision, and consequence. |
| Upstream model or framework | Credit it concisely and state the candidate's integration work. |
| Team project | State the candidate's scope plus compact team attribution. |
| Missing production features | Usually omit; keep in the private report. |
| Current or historical secret | Keep private; remove or rotate separately. |
| Uncertain provenance | Omit the claim and request confirmation privately. |
| Experimental limitation | Mention only when needed to interpret a result; keep it neutral. |
| Repository hygiene issue | Keep private unless it breaks a command or link shown publicly. |

## Tone flags

Review these phrases rather than banning individual words:

- “not production ready”
- “must rotate”
- “future work would add”
- “this demonstrates”
- “useful in an interview”
- long lists of what is missing
- repeated “I built” where code was adapted or integrated

Choose one of three actions: omit, reframe around verified value, or move to the
private delivery report.

## Final review questions

1. What one sentence should the recruiter remember?
2. What repository evidence supports each prominent claim?
3. Which work was authored, integrated, adapted, or shared?
4. What technically interesting interview question does the README invite?
5. Did any paragraph mainly advertise an imperfection rather than the project?
