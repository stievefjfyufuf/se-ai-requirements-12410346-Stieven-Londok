# 02 — Requirements Elicitation

## Elicitation Plan
| Technique | Participants / source | Purpose |
|---|---|---|
| Semi-structured interview | Lecturer, Student, Administrator | Discover goals, workflow, exceptions, and terminology. |
| Document analysis | CASE.md and stakeholder notes | Establish known facts and information boundaries. |
| Scenario walkthrough | Lecturer and Student | Examine assignment creation, submission, grading, and failure paths. |
| Requirements workshop | All primary stakeholders | Resolve deadline, access, reporting, and priority conflicts. |

## Interview Questions
### Lecturer
1. What information is required before an assignment can be published?
2. What should happen when a student attempts to submit after the deadline?
3. Who may change a grade, and what history must be retained?

### Student
1. How do you decide which task needs attention next?
2. What evidence do you need after a submission?
3. Which submission failures must the system explain?

### Administrator
1. How are users associated with roles and courses?
2. Which operational events must reports contain?
3. What load, availability, retention, and access policies are approved?

## Evidence Register
All evidence items `EL-01` through `EL-12` are recorded verbatim in `inputs/interview-answers.md`; `SN-01` through `SN-06` provide initial case evidence.

## Explicit Needs
| ID | Stakeholder | Need | Source |
|---|---|---|---|
| EN-01 | Lecturer | Publish a described assignment with a deadline for one course. | EL-01 |
| EN-02 | Lecturer | Review submissions and record numeric grade and feedback. | EL-02 |
| EN-03 | Lecturer | View completion status by course. | EL-03 |
| EN-04 | Student | View assigned tasks with course, deadline, and status. | EL-04 |
| EN-05 | Student | Submit before deadline and receive recorded confirmation. | EL-05 |
| EN-06 | Student | See submission, grading, and feedback status. | EL-06 |
| EN-07 | Student | See an in-application reminder within 24 hours of deadline. | EL-07 |
| EN-08 | Student | Receive a clear rejection after deadline. | EL-08 |
| EN-09 | Administrator | Maintain users, roles, course assignment, and activation status. | EL-09 |
| EN-10 | Administrator | View operational activity by course. | EL-10 |
| EN-11 | All | Restrict course information and actions by course membership and role. | EL-11, EL-12 |

## Implied Needs
| ID | Interpretation | Status | Validation needed |
|---|---|---|---|
| IN-01 | Grade changes may require an audit history. | ASSUMPTION | Confirm with academic governance. |
| IN-02 | Submission confirmation should contain a timestamp and task reference. | ASSUMPTION | Confirm with students. |
| IN-03 | Deactivated users should lose new-session access while historical records remain. | ASSUMPTION | Confirm retention and security policy. |

## Conflicts and Risks
- `CF-01`: Students may want resubmission flexibility; no resubmission policy is confirmed.
- `CF-02`: Detailed reports increase operational value but may expose student data; report fields and permissions require approval.
- `CF-03`: Reminder usefulness competes with notification fatigue; only a single in-app 24-hour condition is evidenced.

## Open Questions
OQ-01 through OQ-05 remain open. Specification may use assumptions only when visibly labelled and must not convert them into hidden facts.

## Coverage Check
PASS — all three primary stakeholders, all inception goals, core success paths, deadline failure, and access control are covered. Technical NFR thresholds remain explicit academic assumptions pending owner approval.

