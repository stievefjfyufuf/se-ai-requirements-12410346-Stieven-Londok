# GitHub Issues Evidence

Both required issues were created in the final public repository. The matching reusable templates remain available under `.github/ISSUE_TEMPLATE/`.

## Issue 1
**Title:** `[SKILL IMPROVEMENT] Require evidence IDs for every scope item`

**GitHub:** https://github.com/stievefjfyufuf/se-ai-requirements-12410346-Stieven-Londok/issues/1

**Problem:** Initial inception testing allowed plausible but unsupported features such as SMS reminders to appear as scope.  
**Proposed improvement:** Require every stakeholder need and scope item to cite a source ID; otherwise label it `ASSUMPTION` or `OPEN QUESTION`.  
**Affected skill:** `skills/01-inception/SKILL.md`  
**Decision:** Accepted and implemented. Retest passed on the Clinic Appointment System case.

## Issue 2
**Title:** `[CHANGE REQUEST] Add plagiarism detection`

**GitHub:** https://github.com/stievefjfyufuf/se-ai-requirements-12410346-Stieven-Londok/issues/2

**Description:** Analyze submitted files and provide similarity evidence to authorized lecturers.  
**Reason:** Potential support for academic-integrity review.  
**Affected requirements:** FR-03, FR-04, NFR-01 through NFR-04; new FRs and NFRs would be needed.  
**Impact:** Privacy, provider integration, data retention, accuracy, student notice, appeals, cost, schedule, and availability.  
**Proposed decision:** Defer and request more information. See `outputs/reviewed/08-change-request.md`.
