---
name: 01-inception
description: Discover the business problem, goals, stakeholders, scope, assumptions, constraints, and open questions at the start of a requirements engineering project. Use before elicitation or solution specification.
---

# Project Inception and Stakeholder Discovery

## Purpose
Establish a fact-based project foundation by separating the business problem from proposed solutions and identifying goals, stakeholders, scope boundaries, assumptions, constraints, and unanswered questions.

## When to Use
Use at project start, before elicitation, requirements, user stories, or design decisions are produced.

## Inputs
- `CASE.md`
- `inputs/stakeholder-notes.md`
- `inputs/assumptions.md`

## Required Context
Read all three inputs completely. Treat `CASE.md` and source-labelled stakeholder notes as facts. Treat every item in `inputs/assumptions.md` as unverified.

## Workflow
1. Extract the business problem without proposing features.
2. Identify measurable business and stakeholder goals.
3. Classify primary, secondary, and governance stakeholders.
4. Map each stakeholder to needs and evidence source IDs.
5. Define in-scope and out-of-scope boundaries.
6. Record constraints separately from assumptions.
7. Label unsupported but useful propositions as `ASSUMPTION`.
8. Label missing decisions as `OPEN QUESTION` and name the stakeholder who should answer.
9. Run all quality checks; stop if a reliable project boundary cannot be established.

## Output Format
Produce Markdown with: Business Problem, Goals, Stakeholder Register, In Scope, Out of Scope, Constraints, Assumptions, Open Questions, and Inception Quality Check. Use stable IDs `G-xx`, `STK-xx`, `CON-xx`, `ASM-xx`, and `OQ-xx`.

## Rules
- Do not invent stakeholders, policies, deadlines, budgets, integrations, or features.
- Do not express a proposed solution as the business problem.
- Cite at least one source ID for every stakeholder need.
- Mark every unsupported statement as `ASSUMPTION`.
- Keep scope testable: a reader must be able to decide whether an item is inside or outside the project.
- Preserve unresolved conflicts as open questions.

## Quality Checks
- Is the problem described independently of technology?
- Does every goal have an observable success indicator?
- Does every stakeholder have a need and source?
- Are scope, assumptions, constraints, and facts separated?
- Are open questions assigned to an answer owner?
- Are all IDs unique?

## Failure Conditions
Stop and request clarification if `CASE.md` is missing, the business problem is absent, stakeholder sources materially contradict one another, or the scope cannot be bounded. Do not fill gaps with plausible facts.

## Example Invocation
Read `CASE.md`, `skills/01-inception/SKILL.md`, `inputs/stakeholder-notes.md`, and `inputs/assumptions.md`. Execute the skill exactly as written and save the first result to `outputs/raw/inception-ai-output.md`.

## Expected Output Example
`STK-01 | Lecturer | Need: publish assignments with a deadline | Source: SN-01 | Status: FACT`

