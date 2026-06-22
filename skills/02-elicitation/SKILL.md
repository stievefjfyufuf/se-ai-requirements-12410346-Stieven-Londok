---
name: 02-elicitation
description: Plan and synthesize requirements elicitation using interviews, document analysis, source IDs, explicit needs, implied needs, assumptions, and open questions. Use after project inception.
---

# Requirements Elicitation

## Purpose
Collect and organize stakeholder evidence without converting guesses into requirements.

## When to Use
Use after inception has identified stakeholders and scope, and before requirements are specified.

## Inputs
- `CASE.md`
- `outputs/reviewed/01-inception.md`
- `inputs/stakeholder-notes.md`
- `inputs/interview-answers.md`
- `inputs/assumptions.md`

## Required Context
Read the inception scope and open questions first. Preserve the source IDs already assigned in the input files.

## Workflow
1. Identify evidence gaps by stakeholder and topic.
2. Select appropriate elicitation techniques and explain why each fits.
3. Prepare neutral, open-ended interview questions grouped by stakeholder.
4. Extract explicit needs from each source as `EN-xx`.
5. Record implied needs as `IN-xx`; do not treat them as confirmed.
6. Identify conflicts, constraints, risks, and unresolved questions.
7. Link every finding to a source ID such as `EL-xx` or `SN-xx`.
8. Summarize coverage against inception goals and stakeholders.
9. Run quality checks and stop if evidence is insufficient for specification.

## Output Format
Produce Markdown with: Elicitation Plan, Interview Questions, Evidence Register, Explicit Needs, Implied Needs, Conflicts, Open Questions, and Coverage Check.

## Rules
- Do not write functional requirements yet.
- Do not use leading questions that assume a preferred solution.
- Keep explicit and implied needs separate.
- Mark unsupported interpretations as `ASSUMPTION`.
- Never remove a conflict merely to make the output consistent.
- Every finding must have a stakeholder and source ID.

## Quality Checks
- Are all primary stakeholders covered?
- Can every finding be traced to evidence?
- Are questions neutral and answerable?
- Are implied needs clearly unconfirmed?
- Are contradictions and missing information visible?
- Is there enough evidence to proceed to specification?

## Failure Conditions
Stop and request clarification when interview evidence is missing for a primary stakeholder, source IDs are absent or duplicated, material answers conflict without an owner to resolve them, or inception scope is unavailable.

## Example Invocation
Read the required context and execute `skills/02-elicitation/SKILL.md`. Save the unedited first response to `outputs/raw/elicitation-ai-output.md`.

## Expected Output Example
`EN-03 | Student | Need confirmation after a successful submission | Source: EL-05 | Confidence: Confirmed`

