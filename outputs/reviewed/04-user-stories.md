# 04 — User Stories and Acceptance Criteria

## US-01 — Publish an Assignment
**Story:** As a lecturer, I want to publish an assignment with a deadline for my course so that students know what work is required.  
**Linked requirement:** FR-01

- **AC-01:** Given the lecturer is assigned to the course and enters a title, description, and future deadline, when they publish, then the assignment is stored and visible to assigned students.
- **AC-02:** Given the lecturer is not assigned to the course, when they attempt to publish, then the system denies the action and no assignment is created.

## US-02 — View Work and Reminder
**Story:** As a student, I want to view my assignments and approaching deadlines so that I can plan my work.  
**Linked requirements:** FR-02, FR-07

- **AC-03:** Given a student is assigned to two courses, when they open the task list, then only assignments from those courses appear with course, deadline, and status.
- **AC-04:** Given an assignment is unsubmitted and due in 24 hours or less, when the student opens the application, then an in-application reminder is displayed for that assignment.

## US-03 — Submit Work
**Story:** As a student, I want to submit my file before the deadline and receive a receipt so that I have evidence of submission.  
**Linked requirement:** FR-03

- **AC-05:** Given an assigned student submits a file at or before the deadline and persistence succeeds, when processing completes, then a receipt records the task, student, and server timestamp.
- **AC-06:** Given the server time is later than the deadline, when the student attempts a normal submission, then it is rejected, the reason is shown, and no receipt is created.

## US-04 — Grade a Submission
**Story:** As a lecturer, I want to grade a student's submission and provide feedback so that the student understands the assessment.  
**Linked requirement:** FR-04

- **AC-07:** Given the assigned lecturer opens a recorded submission and enters a numeric grade and feedback, when saving succeeds, then both values are associated with that submission.
- **AC-08:** Given a lecturer is not assigned to the course, when they attempt to view or grade the submission, then access is denied and no grade changes.

## US-05 — Track Assignment Status
**Story:** As a student, I want to see the status and feedback for each assignment so that I know what action remains.  
**Linked requirement:** FR-05

- **AC-09:** Given no receipt exists for an assignment, when the student views it, then its status is `not submitted`.
- **AC-10:** Given a grade and written feedback are recorded, when the student views the assignment, then its status and the authorized result are displayed.

## US-06 — Administer Courses and Monitor Activity
**Story:** As an administrator, I want to manage course participation and view course activity so that authorized users can operate and support can identify outstanding work.  
**Linked requirements:** FR-06, FR-08

- **AC-11:** Given valid user, role, and course data, when an administrator assigns the user, then the active course membership is stored and governs subsequent access.
- **AC-12:** Given an authorized administrator selects a course, when requesting its activity report, then assignments and enrolled students' submission statuses are shown; users outside the course cannot access the report.

## Coverage Check
All FRs are linked: US-01 → FR-01; US-02 → FR-02/FR-07; US-03 → FR-03; US-04 → FR-04; US-05 → FR-05; US-06 → FR-06/FR-08. Each story has two uniquely identified, testable acceptance criteria including relevant failure behaviour.

