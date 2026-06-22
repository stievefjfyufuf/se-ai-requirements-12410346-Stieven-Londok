# Requirements Traceability Matrix

| Requirement | Stakeholder | Source | User Story | Acceptance Criteria | Use Case | Priority |
|---|---|---|---|---|---|---|
| FR-01 | Lecturer | EL-01, EL-12 | US-01 | AC-01, AC-02 | UC-01 | Must |
| FR-02 | Student | EL-04, EL-11 | US-02 | AC-03, AC-04 | UC-02 | Must |
| FR-03 | Student | EL-05, EL-11 | US-03 | AC-05, AC-06 | UC-03 | Must |
| FR-04 | Lecturer | EL-02, EL-12 | US-04 | AC-07, AC-08 | UC-04 | Must |
| FR-05 | Student | EL-06 | US-05 | AC-09, AC-10 | UC-05 | Must |
| FR-06 | Administrator | EL-09 | US-06 | AC-11, AC-12 | UC-06 | Must |
| FR-07 | Student | EL-07 | US-02 | AC-04 | UC-07 | Should |
| FR-08 | Lecturer, Administrator | EL-03, EL-10, EL-11 | US-06 | AC-12 | UC-08 | Should |

## NFR Traceability
| Requirement | Source / assumption | Related FRs / use cases | Verification |
|---|---|---|---|
| NFR-01 | EL-11, EL-12 | All role-bound FRs; UC-01–UC-08 | Authorization matrix |
| NFR-02 | ASM-05 | FR-02; UC-02 | 15-minute load test |
| NFR-03 | ASM-06 | All service use cases | Monthly monitoring report |
| NFR-04 | SN-05 | FR-01, FR-03, FR-04; UC-01, UC-03, UC-04 | Fault-injection rollback tests |

## Integrity Check
PASS — no orphan FR exists; each FR has a stakeholder, source, story, criterion, use case, and priority. Provisional NFR evidence remains visibly labelled.

