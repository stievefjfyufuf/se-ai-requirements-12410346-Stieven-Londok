# 06 — Use-Case Model

## Actors
| Actor | Responsibility |
|---|---|
| Lecturer | Publish assignments, review submissions, grade, provide feedback, view course reports. |
| Student | View assignments, submit work, receive reminders, track status and feedback. |
| Administrator | Manage users and course membership, view operational course reports. |

## Use Cases
| ID | Use case | Primary actor | Preconditions | Success outcome | Related requirements |
|---|---|---|---|---|---|
| UC-01 | Publish assignment | Lecturer | Lecturer is assigned to course. | Assignment is visible to assigned students. | FR-01, NFR-01 |
| UC-02 | View assigned tasks | Student | Student has active course membership. | Task list shows course, deadline, and status. | FR-02 |
| UC-03 | Submit assignment | Student | Assignment exists; server time is not after deadline. | File and receipt are recorded atomically. | FR-03, BR-01, NFR-04 |
| UC-04 | Grade submission | Lecturer | Submission exists; lecturer is assigned to course. | Grade and feedback are recorded. | FR-04, BR-02 |
| UC-05 | Track status and feedback | Student | Student owns the submission context. | Current status and authorized result appear. | FR-05 |
| UC-06 | Manage users and courses | Administrator | Administrator is authenticated and active. | User role and course membership are stored. | FR-06, NFR-01 |
| UC-07 | Receive deadline reminder | Student | Task is unsubmitted and due within 24 hours. | In-app reminder appears. | FR-07 |
| UC-08 | View course activity report | Lecturer, Administrator | User is authorized for the course. | Assignment and submission status report appears. | FR-08, NFR-01 |

## Main Scenario — UC-03 Submit Assignment
1. Student opens an assigned task.
2. System verifies active course membership and current server time.
3. Student selects a file and confirms submission.
4. System stores the file reference and submission receipt as one transaction.
5. System displays task, student, and server timestamp confirmation.

## Alternate and Failure Flows
- **A1 — Deadline passed:** Reject the normal submission, explain the deadline condition, and create no receipt.
- **A2 — Unauthorized course:** Deny access and reveal no submission data.
- **A3 — Persistence failure:** Roll back the transaction and show that no submission was recorded.

## Diagram
See [use-case-diagram.png](../../diagrams/use-case-diagram.png) and editable [use-case-diagram.drawio](../../diagrams/use-case-diagram.drawio).

