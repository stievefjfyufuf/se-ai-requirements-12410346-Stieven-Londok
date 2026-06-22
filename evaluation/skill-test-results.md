# Skill Test Results

## Test Strategy
Two skills were applied to cases outside the Student Task Management System to test reusability and failure behaviour. Tests used only the stated input; expected behaviour was evaluated against each skill's rules and quality checks.

## Test 1 — Inception Skill on Clinic Appointment System

### Input
“A clinic receives appointments by telephone. Patients report long wait times and receptionists sometimes double-book doctors. Known stakeholders: patient, receptionist, doctor. Budget, integration, and appointment-cancellation rules are unknown.”

### Initial Result
The skill identified the scheduling problem and stakeholders but originally allowed the AI to recommend SMS reminders and calendar integration as scope facts.

### Failure Cause
The original rule prohibited invented features but did not require every scope item and stakeholder need to cite a source.

### Skill Improvement
Added mandatory evidence IDs for stakeholder needs, required unsupported propositions to use `ASSUMPTION`, and strengthened the failure condition when scope cannot be bounded.

### Retest Result
PASS — appointment booking and double-booking prevention remained fact-based; SMS and calendar integration became open questions rather than requirements.

## Test 2 — Specification Skill on Library Reservation System

### Input Evidence
- `LIB-01`: A member can reserve an available book.
- `LIB-02`: A reservation expires if not collected by an approved pickup deadline.
- `LIB-03`: A librarian can view active and expired reservations.
- No performance threshold, pickup duration, or notification channel is provided.

### Initial Result
The AI produced “The system shall respond quickly,” invented a 48-hour pickup duration, and added email notification.

### Failure Cause
The original workflow asked for NFRs and acceptance criteria but did not block generation when targets lacked an approved basis.

### Skill Improvement
Required every NFR to include metric, threshold, operating condition, and verification method; added a failure condition for unapproved NFR targets; required every feature to trace to confirmed evidence.

### Retest Result
PASS WITH OPEN QUESTIONS — source-backed reservation and librarian requirements were produced; pickup duration, notification channel, and performance target were returned as blocking questions instead of invented facts.

## Summary
| Skill | Different case | Initial outcome | Revision | Retest |
|---|---|---|---|---|
| 01-inception | Clinic Appointment System | Unsupported scope leaked in | Mandatory source IDs and stronger assumption gate | Pass |
| 03-specification | Library Reservation System | Values and features invented | Evidence gate and measurable NFR contract | Pass with open questions |

