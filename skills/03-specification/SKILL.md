---
name: 03-specification
description: Convert elicitation evidence into uniquely identified, measurable, testable, and traceable functional requirements, non-functional requirements, business rules, user stories, and acceptance criteria.
---

# Requirements Elaboration and Specification

## Purpose
Transform validated stakeholder evidence into a precise, testable requirements specification and user-story set.

## When to Use
Use after elicitation evidence has sufficient coverage and before prioritization.

## Inputs
- `CASE.md`
- `outputs/reviewed/01-inception.md`
- `outputs/reviewed/02-elicitation.md`
- `inputs/interview-answers.md`

## Required Context
Read all confirmed needs, scope boundaries, constraints, conflicts, and open questions. Only confirmed evidence may become a baseline requirement.

## Workflow
1. Convert confirmed capabilities into atomic functional requirements `FR-xx` using “The system shall”.
2. Specify measurable quality attributes as `NFR-xx` with metric, threshold, operating condition, and verification method.
3. Define source-backed business rules `BR-xx`.
4. Detect duplicates, bundled requirements, solution bias, and ambiguous words.
5. Create user stories `US-xx` linked to functional requirements.
6. Create at least two Given/When/Then acceptance criteria per story with IDs `AC-xx`.
7. Include negative or failure behaviour where relevant.
8. Verify bidirectional traceability to stakeholder and elicitation source.
9. Run quality checks before producing both required output files.

## Output Format
Create `03-requirements.md` containing scope reference, functional requirements, non-functional requirements, business rules, assumptions, and quality summary. Create `04-user-stories.md` containing user stories, linked FR IDs, acceptance criteria, and story coverage.

## Rules
- Do not add a feature without confirmed source evidence.
- Use one obligation per requirement.
- Avoid “fast”, “easy”, “secure”, “user-friendly”, “etc.”, and other unmeasured terms.
- Keep implementation design out unless it is an explicit constraint.
- Every FR must include stakeholder, source, rationale, and verification method.
- Every NFR must be measurable and testable.
- Every acceptance criterion must have a unique ID and an observable result.

## Quality Checks
- Are requirements correct, complete, consistent, feasible, necessary, unambiguous, and testable?
- Is every FR atomic and uniquely identified?
- Does every FR trace to confirmed evidence and at least one user story or justified system use case?
- Does each user story have at least two acceptance criteria?
- Do acceptance criteria cover success and relevant failure paths?
- Are all minimum counts satisfied without padding or duplicates?

## Failure Conditions
Stop if confirmed evidence does not support the minimum requirement set, a requirement depends on an unresolved high-impact conflict, a measurable NFR target has no approved basis, or traceability cannot be established. Return the blocking open questions instead of inventing values.

## Example Invocation
Execute `skills/03-specification/SKILL.md` using the reviewed inception and elicitation outputs. Save the first response unchanged to `outputs/raw/requirements-ai-output.md`.

## Expected Output Example
`FR-03 | The system shall accept a student's file submission for an assigned task before its deadline and record a submission receipt. | Source: EL-05 | Verification: Functional test`

