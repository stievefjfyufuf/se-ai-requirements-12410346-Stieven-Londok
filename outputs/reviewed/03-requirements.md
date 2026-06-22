# 03 — Requirements Specification

## Functional Requirements
| ID | Requirement | Stakeholder | Source | Rationale | Verification |
|---|---|---|---|---|---|
| FR-01 | The system shall allow a lecturer assigned to a course to create and publish an assignment containing a title, description, and deadline for that course. | Lecturer | EL-01, EL-12 | Establishes work to be completed. | Role-based functional test |
| FR-02 | The system shall show each student a list of assignments for their assigned courses including course, deadline, and current status. | Student | EL-04, EL-11 | Provides one actionable workload view. | Functional and access test |
| FR-03 | The system shall accept a file submission from an assigned student before the assignment deadline and record a receipt containing task, student, and submission timestamp. | Student | EL-05, EL-11 | Creates reliable evidence of submission. | Boundary and persistence test |
| FR-04 | The system shall allow the assigned lecturer to view a student's submission and record a numeric grade with written feedback. | Lecturer | EL-02, EL-12 | Supports assessment and feedback. | Role-based functional test |
| FR-05 | The system shall show a student each assignment's status as not submitted, submitted, graded, or returned with feedback, based on recorded events. | Student | EL-06 | Gives progress visibility. | State-transition test |
| FR-06 | The system shall allow an administrator to create, update, deactivate, and assign users to courses with a lecturer, student, or administrator role. | Administrator | EL-09 | Maintains authorized participation. | CRUD, role, and deactivation test |
| FR-07 | The system shall display an in-application reminder to a student when an unsubmitted assignment deadline is within the next 24 hours. | Student | EL-07 | Reduces overlooked deadlines without assuming external channels. | Time-boundary test |
| FR-08 | The system shall provide authorized lecturers and administrators a course report listing assignments and each enrolled student's submission status. | Lecturer, Administrator | EL-03, EL-10, EL-11 | Supports follow-up and operations. | Report content and authorization test |

## Non-Functional Requirements
| ID | Requirement | Quality attribute | Basis | Verification |
|---|---|---|---|---|
| NFR-01 | The system shall deny access to course assignments, submissions, grades, and reports when the authenticated user's active role is not assigned to that course; all authorization tests in the approved access matrix shall pass. | Security | EL-11, EL-12 | Automated authorization matrix |
| NFR-02 | Under a test load of 500 concurrent authenticated users, at least 95% of task-list requests shall complete within 3 seconds over a 15-minute load test. | Performance | ASM-05 | Load test; target requires owner approval |
| NFR-03 | The service shall achieve at least 99.5% monthly availability excluding announced maintenance, measured by one-minute external health checks. | Reliability | ASM-06 | Monitoring report; target requires owner approval |
| NFR-04 | Assignment publication, submission receipt creation, and grade update shall be atomic: if persistence fails, no partial business record shall remain; all transaction rollback integration tests shall pass. | Data integrity | SN-05 | Fault-injection integration test |

## Business Rules
| ID | Rule | Source / status |
|---|---|---|
| BR-01 | A normal submission is accepted only when the recorded server time is not later than the assignment deadline; otherwise it is rejected with an explanation. | EL-05, EL-08 |
| BR-02 | Only the lecturer assigned to the course may publish its assignments or record and change its grades. | EL-12 |

## Assumptions Requiring Approval
- NFR-02 uses `ASM-05`; load and threshold are provisional academic targets.
- NFR-03 uses `ASM-06`; availability and maintenance exclusion require owner approval.
- Numeric grade boundaries remain open; FR-04 does not invent a 0–100 validation rule.

## Quality Summary
PASS with documented assumptions — 8 atomic FRs, 4 measurable NFRs, and 2 source-backed business rules are uniquely identified, testable, and traceable. No chat, plagiarism, email, or SMS feature is included.

