# 01 — Project Inception and Stakeholder Discovery

## Business Problem
Lecturers, students, and administrators need a consistent way to coordinate coursework tasks and preserve trustworthy records of creation, submission, grading, and status. The challenge is not merely storing files: each stakeholder must see and change only the information appropriate to their course role while deadlines and academic records remain reliable.

## Goals
| ID | Goal | Success indicator | Source |
|---|---|---|---|
| G-01 | Enable lecturers to manage the assignment lifecycle. | A lecturer can publish a task and record grade and feedback for an assigned course. | SN-01, SN-02 |
| G-02 | Enable students to complete and track assigned work. | A student can locate an assigned task, submit before deadline, and observe status. | SN-03 |
| G-03 | Enable controlled academic administration. | An administrator can maintain users, courses, roles, and configuration. | SN-04 |
| G-04 | Preserve dependable and usable service quality. | Approved measurable security, performance, reliability, usability, and integrity criteria pass validation. | SN-05 |

## Stakeholder Register
| ID | Stakeholder | Classification | Need | Source |
|---|---|---|---|---|
| STK-01 | Lecturer | Primary | Create tasks, set deadlines, inspect submissions, grade, provide feedback, and monitor course completion. | SN-01, SN-02, SN-06 |
| STK-02 | Student | Primary | Find tasks, understand deadlines, submit work, receive confirmation, and track results. | SN-03 |
| STK-03 | Administrator | Primary / governance | Maintain access, courses, configuration, and operational reporting. | SN-04, SN-06 |
| STK-04 | Campus governance | Secondary / governance | Ensure quality attributes and academic rules are satisfied. | SN-05 |

## In Scope
- Assignment creation and publication for a course.
- Task list, deadline visibility, file submission, and submission confirmation.
- Submission review, grading, written feedback, and status tracking.
- User, role, and course administration.
- Course-level task and submission reporting.
- Access control, measurable performance, availability, and data-integrity criteria.

## Out of Scope
- Real-time chat, video conferencing, attendance, tuition payment, and learning-content authoring.
- Plagiarism detection until separately evaluated through change control.
- Email or SMS notifications without a confirmed requirement.
- Mobile-native applications; the delivery channel is not specified.

## Constraints
| ID | Constraint | Source |
|---|---|---|
| CON-01 | The system must support lecturer, student, and administrator responsibilities. | CASE.md |
| CON-02 | Security, performance, reliability, usability, and data integrity must be addressed. | SN-05 |
| CON-03 | Unsupported information must remain an assumption or open question. | Assignment rule |

## Assumptions
ASM-01 through ASM-06 remain unapproved unless explicitly used as validation targets in this academic baseline. See `inputs/assumptions.md`.

## Open Questions
| ID | Question | Owner | Impact |
|---|---|---|---|
| OQ-01 | Which identity provider and role source are authoritative? | Administrator | Security and integration |
| OQ-02 | Which file types, size limits, and resubmission policy apply? | Lecturer / Administrator | Submission rules |
| OQ-03 | What grading scale and grade-change audit rules apply? | Academic governance | Business rules |
| OQ-04 | What approved load and availability targets apply? | Operations / Product owner | NFR baseline |
| OQ-05 | What report fields and export formats are needed? | Lecturer / Administrator | Reporting scope |

## Inception Quality Check
PASS — the business problem is solution-neutral; all stakeholders have source-backed needs; scope boundaries, constraints, assumptions, and open questions are separate; identifiers are unique.

