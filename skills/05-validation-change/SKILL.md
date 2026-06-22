---
name: 05-validation-change
description: Validate requirements for clarity, completeness, consistency, feasibility, testability, and traceability; assess requirement changes using impact analysis and controlled baseline decisions.
---

# Requirements Validation and Change Management

## Purpose
Establish a reviewed requirement baseline and prevent uncontrolled changes from breaking scope, traceability, or dependent artefacts.

## When to Use
Use after prioritization and whenever a change request is proposed against the baseline.

## Inputs
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/05-prioritization.md`
- `outputs/reviewed/06-use-case.md`
- `outputs/reviewed/requirements-traceability.md`
- A proposed change request

## Required Context
Read all linked artefacts and treat their IDs as a single baseline. Identify the current baseline version and change requester.

## Workflow
1. Validate selected requirements for correctness, clarity, completeness, consistency, feasibility, necessity, testability, and traceability.
2. Record each defect with severity, evidence, and correction.
3. Recheck all affected links after correction.
4. Assign the validated baseline a version and approval status.
5. Register a change request `CR-xx` with requester, reason, source, and proposed modification.
6. Analyze impact on scope, stakeholders, requirements, stories, criteria, use cases, NFRs, priority, risks, and schedule.
7. Recommend Approve, Reject, Defer, or Request More Information with rationale.
8. Update the baseline only after an explicit decision; preserve the previous version in history.
9. Run final quality and traceability checks.

## Output Format
Create `07-validation.md` with validation matrix, corrections, residual issues, and baseline decision. Create `08-change-request.md` with change register, impact analysis, alternatives, decision, and required updates.

## Rules
- Do not mark a requirement valid without recorded checks.
- Do not silently edit IDs or overwrite baseline history.
- A change request is not approved merely because it is valuable.
- Identify all affected artefacts and owners.
- Keep proposed changes separate from approved baseline content.
- Label missing impact data as `OPEN QUESTION`.

## Quality Checks
- Were at least five requirements validated across all quality dimensions?
- Does each correction preserve or deliberately update traceability?
- Is the baseline version and status explicit?
- Does the change analysis cover direct and downstream impacts?
- Is the decision supported by value, cost, risk, dependency, and evidence?
- Are affected artefact updates listed?

## Failure Conditions
Stop if the current baseline version is unknown, traceability data is missing, the requester or reason is absent, affected requirements cannot be identified, or decision authority is unavailable. Return `Request More Information` rather than guessing.

## Example Invocation
Execute `skills/05-validation-change/SKILL.md` against the prioritized baseline and proposed change. Save the first response unchanged to `outputs/raw/validation-ai-output.md`.

## Expected Output Example
`CR-01 | Add plagiarism detection | Decision: Defer | Reason: no approved provider, privacy assessment, accuracy threshold, or budget evidence`

