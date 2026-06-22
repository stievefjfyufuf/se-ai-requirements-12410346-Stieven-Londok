# 08 — Change Request

## Change Register
| Field | Value |
|---|---|
| Change ID | CR-01 |
| Title | Add plagiarism detection |
| Requester | Proposed by lecturer perspective; formal owner confirmation pending |
| Date | 22 June 2026 |
| Baseline | 1.0 |
| Proposed priority | Not assigned pending evidence |
| Status | Deferred — more information required |

## Description and Reason
Compare submitted files against an approved corpus or service and present similarity evidence to authorized lecturers. The proposed value is support for academic-integrity review; the system must not automatically equate similarity with misconduct.

## Impact Analysis
| Area | Impact |
|---|---|
| Scope | Adds analysis workflow beyond the validated task-management baseline. |
| Stakeholders | Lecturer and administrator workflows expand; students require notice, transparency, and possibly an appeal path. |
| Functional requirements | Would add analysis request, result viewing, retry/failure, and authorization requirements; FR-03 and FR-04 links would change. |
| Non-functional requirements | Adds privacy, security, performance, availability, explainability, and accuracy thresholds. |
| Data | Requires approved corpus, file transfer rules, retention, deletion, and provider-processing terms. |
| User stories / acceptance criteria | Requires new stories and criteria for unavailable service, unsupported file, false-positive handling, and authorized result access. |
| Use cases | Adds plagiarism analysis and review-result use cases. |
| Priority and schedule | Cost and integration dependency are unknown; existing Must baseline should not be delayed without approval. |
| Risk | Privacy breach, vendor lock-in, false accusation, poor accuracy, service outage, and unclear appeals process. |

## Alternatives
1. Defer automated detection and retain lecturer manual review.
2. Run a limited non-production evaluation with anonymized samples after governance approval.
3. Integrate a provider only after accuracy, privacy, cost, retention, and appeals criteria are approved.

## Decision
**DEFER / REQUEST MORE INFORMATION.** The raw AI recommendation to approve is rejected because impact is material and required evidence is absent.

## Information Required for Reconsideration
- Authorized decision owner and academic-integrity policy.
- Approved provider or corpus and lawful processing basis.
- Similarity accuracy measures and human-review rule.
- Student notice, dispute, and appeal process.
- Cost, schedule, availability, retention, and security assessment.

## Required Updates if Later Approved
Update CASE scope, inception assumptions, elicitation evidence, FR/NFR/BR sets, user stories, acceptance criteria, priorities, use cases, traceability matrix, test plan, baseline version, and `CHANGELOG.md`.

