# 05 — Negotiation and MoSCoW Prioritization

## Decision Criteria
Priority considers core outcome, business value, stakeholder reach, dependency, security or integrity risk, and whether the first release remains coherent without the requirement.

## Conflict Log
| ID | Conflict | Decision | Rationale |
|---|---|---|---|
| CF-01 | Submission flexibility versus deadline enforcement | Keep normal deadline rejection; route exceptions to future policy. | EL-08 confirms explanation, but no late-submission authority is defined. |
| CF-02 | Reporting value versus student-data exposure | Limit reports to authorized course roles. | EL-03/EL-10 value reports; EL-11 requires course restriction. |
| CF-03 | Reminder value versus release scope | Retain one in-app reminder as Should. | Useful but not required for the core create-submit-grade workflow. |

## Dependency Map
- FR-03 depends on FR-01 and FR-06.
- FR-04 depends on FR-03 and FR-06.
- FR-05 depends on FR-01 and submission/grading events from FR-03/FR-04.
- FR-07 depends on FR-01, FR-02, and current submission state.
- FR-08 depends on FR-01, FR-03, and FR-06.

## MoSCoW Table
| Requirement | Priority | Evidence-based rationale | Dependencies |
|---|---|---|---|
| FR-01 | Must | No assignment workflow exists without lecturer publication. | FR-06 for authorization |
| FR-02 | Must | Students cannot discover required work without an assigned task view. | FR-01, FR-06 |
| FR-03 | Must | Submission is a primary student outcome and must create reliable evidence. | FR-01, FR-06 |
| FR-04 | Must | Assessment and feedback are explicit lecturer outcomes. | FR-03, FR-06 |
| FR-05 | Must | Status closes the student workflow and prevents uncertainty about recorded events. | FR-01, FR-03, FR-04 |
| FR-06 | Must | Course-role membership is a prerequisite for correct access and ownership. | None |
| FR-07 | Should | Deadline reminders add value but the core workflow remains usable through visible deadlines. | FR-01, FR-02, FR-03 |
| FR-08 | Should | Reporting supports follow-up and operations but is not required to create, submit, and grade one task. | FR-01, FR-03, FR-06 |

## Trade-off Decisions
- `DEC-01 Accepted`: Keep FR-07 in-app only; external channels are not evidenced.
- `DEC-02 Accepted`: Keep FR-08 at course level and authorization-bound.
- `DEC-03 Deferred`: Resubmission and late-submission exceptions require an approved academic policy.

## Quality Check
PASS — all eight FRs are prioritized exactly once; Must requirements create a coherent authorized assignment lifecycle; prerequisites are not ranked below dependent Must items; conflicts and deferrals remain visible.

