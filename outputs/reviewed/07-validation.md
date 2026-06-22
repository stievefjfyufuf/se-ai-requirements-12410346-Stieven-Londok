# 07 — Requirements Validation

## Validation Method
Each selected requirement was reviewed for clarity, completeness, consistency, feasibility, necessity, testability, and traceability. Validation uses source inspection, walkthroughs, acceptance-criteria comparison, and planned functional or quality tests.

## Validation Matrix
| Item | Defect in raw draft | Correction in reviewed baseline | Result |
|---|---|---|---|
| FR-01 | “Manage assignments” bundled unspecified actions. | Limited to create and publish with title, description, deadline, course role, source, and test. | Pass |
| FR-03 | Duplicate upload requirements; “quickly” was ambiguous. | Merged into one atomic submission-and-receipt obligation with deadline boundary and verification. | Pass |
| FR-04 | Grading, feedback, and reporting were bundled. | Kept grade and feedback in FR-04; separated reporting into FR-08. | Pass |
| FR-06 | “Manage everything” was unbounded. | Enumerated create, update, deactivate, role, and course assignment operations. | Pass |
| NFR-01 | “Secure” lacked a condition or oracle. | Added course-role access matrix and 100% authorization-test pass condition. | Pass |
| NFR-02 | “Fast” had no metric. | Added 95th-percentile, 3-second, 500-user, 15-minute load-test target and assumption label. | Pass with assumption |
| NFR-03 | “Always available” was impossible and unmeasured. | Added 99.5% monthly target, exclusion, and monitoring method. | Pass with assumption |
| NFR-04 | Data integrity was named but unspecified. | Added atomic transaction and rollback-test criterion. | Pass |

## Cross-Artefact Checks
- All FR-01 through FR-08 occur exactly once in the requirement and priority tables.
- Every FR links to at least one elicitation source and one user story.
- AC-01 through AC-12 are unique and cover all six user stories.
- UC-01 through UC-08 cover all FRs.
- Priorities respect dependency order and access-control prerequisites.

## Residual Issues
- `OQ-02`: file formats, size, and resubmission policy remain unresolved.
- `OQ-03`: numeric grade range and grade-change audit policy remain unresolved.
- `OQ-04`: owners must approve NFR-02 and NFR-03 target values before production commitment.
- `OQ-05`: export formats and additional report fields remain unresolved.

## Baseline Decision
`Baseline 1.0 — CONDITIONALLY APPROVED FOR ASSIGNMENT SUBMISSION.` Core functional scope is validated. Provisional NFR targets are transparent academic assumptions, not undisclosed production commitments.

