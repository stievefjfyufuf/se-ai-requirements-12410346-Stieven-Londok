---
name: 04-prioritization
description: Negotiate stakeholder conflicts, analyze dependencies and trade-offs, and assign justified MoSCoW priorities to functional requirements while preserving decision traceability.
---

# Negotiation and Prioritization

## Purpose
Produce an explainable, dependency-aware priority baseline instead of an unsupported ranking.

## When to Use
Use after functional requirements and user stories exist and before validation freezes a baseline.

## Inputs
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/02-elicitation.md`
- `outputs/reviewed/01-inception.md`

## Required Context
Read business goals, stakeholder needs, all FR IDs, dependencies, risks, and recorded conflicts.

## Workflow
1. Build a dependency map for all functional requirements.
2. Identify stakeholder conflicts and competing quality concerns.
3. Evaluate business value, user impact, risk, dependency, and delivery necessity.
4. Assign exactly one MoSCoW category to every FR.
5. Explain each priority using evidence; do not use priority labels as their own justification.
6. Record trade-offs, rejected alternatives, and decision owners.
7. Check that Must requirements form a coherent minimum viable service.
8. Run quality checks and preserve unresolved decisions.

## Output Format
Produce Markdown with: Decision Criteria, Conflict Log, Dependency Map, MoSCoW Table, Trade-off Decisions, Deferred Items, and Quality Check.

## Rules
- Prioritize every FR exactly once.
- `Must` means the release is not viable, compliant, or coherent without it.
- Do not classify every item as Must.
- A dependent requirement cannot outrank an indispensable prerequisite without explanation.
- Keep stakeholder preference separate from final decision.
- Record rationale, source, dependencies, and decision status.

## Quality Checks
- Does every FR have one category and evidence-based rationale?
- Are dependencies consistent with assigned priorities?
- Are stakeholder conflicts explicitly resolved or left open?
- Do Must items represent a coherent baseline?
- Are trade-offs and decision owners visible?
- Are no FR IDs missing or duplicated?

## Failure Conditions
Stop if the requirements list is incomplete, priorities lack business goals, a critical conflict has no authorized decision owner, or dependencies make the proposed baseline infeasible.

## Example Invocation
Execute `skills/04-prioritization/SKILL.md` using reviewed requirements, user stories, elicitation, and inception outputs. Save the first response unchanged in `outputs/raw/prioritization-ai-output.md`.

## Expected Output Example
`FR-03 | Must | Core student submission outcome; depends on FR-01 | Evidence: G-02, EL-05 | Decision: Accepted`

