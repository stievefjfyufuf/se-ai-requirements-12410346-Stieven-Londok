# AI Output Review

## Review Method
Each raw output was preserved unchanged, compared with source evidence and its skill quality checks, and then corrected in `outputs/reviewed/`. Corrections are human-owned baseline decisions.

## Skill 1 — Project Inception and Stakeholder Discovery
**Raw file:** `outputs/raw/inception-ai-output.md`  
**Final file:** `outputs/reviewed/01-inception.md`

### Problems Found
1. Invented parents and IT support as stakeholders.
2. Added chat, attendance, plagiarism, email, mobile, SSO, AWS, and a three-month schedule without sources.
3. Described a technical solution instead of the business problem.
4. Asked a low-value visual-design question while policy gaps remained hidden.

### Student Corrections
Removed unsupported facts, separated scope from assumptions, added source-backed stakeholder needs, and registered OQ-01 through OQ-05 with owners.

## Skill 2 — Requirements Elicitation
**Raw file:** `outputs/raw/elicitation-ai-output.md`  
**Final file:** `outputs/reviewed/02-elicitation.md`

### Problems Found
1. Interview questions were leading and assumed email, plagiarism detection, and mobile delivery.
2. Findings lacked source and stakeholder IDs.
3. Explicit needs, implied needs, conflicts, and assumptions were mixed.
4. “Secure” and “fast” were treated as usable findings without eliciting measures.

### Student Corrections
Replaced leading questions with neutral workflow and exception questions, created evidence-linked needs EN-01 through EN-11, and preserved conflicts and implied needs separately.

## Skill 3 — Requirements Elaboration and Specification
**Raw file:** `outputs/raw/requirements-ai-output.md`  
**Final files:** `outputs/reviewed/03-requirements.md`, `outputs/reviewed/04-user-stories.md`

### Problems Found
1. Used ambiguous terms: “quickly”, “fast”, “secure”, “user-friendly”, and “always”.
2. Duplicated submission requirements.
3. Bundled grading, feedback, and reporting.
4. Added unsupported chat and plagiarism features.
5. “Manage everything” was unbounded.
6. The single acceptance criterion had no boundary or failure behaviour.

### Student Corrections
Created 8 atomic FRs, 4 measurable NFRs, 2 business rules, 6 stories, and 12 Given/When/Then criteria; added sources, verification methods, authorization, deadline rejection, rollback, and transparent assumption labels.

## Skill 4 — Negotiation and Prioritization
**Raw file:** `outputs/raw/prioritization-ai-output.md`  
**Final file:** `outputs/reviewed/05-prioritization.md`

### Problems Found
1. Classified everything as Must without release-necessity analysis.
2. Prioritized unsupported features.
3. Ignored dependencies and stakeholder conflicts.
4. Used “Medium”, which is not a MoSCoW category.

### Student Corrections
Prioritized every valid FR exactly once, mapped dependencies, recorded three conflicts, retained six coherent Must items, and assigned two source-supported Should items.

## Skill 5 — Requirements Validation and Change Management
**Raw file:** `outputs/raw/validation-ai-output.md`  
**Final files:** `outputs/reviewed/07-validation.md`, `outputs/reviewed/08-change-request.md`

### Problems Found
1. Declared requirements valid without recorded checks.
2. Accepted unmeasured “fast” and “secure” language.
3. Approved plagiarism detection without privacy, accuracy, provider, cost, policy, or schedule analysis.
4. Claimed the change had no downstream impact.

### Student Corrections
Validated eight representative requirements across quality dimensions, recorded corrections and residual issues, assigned baseline 1.0, and deferred CR-01 pending required evidence and authority.

## Overall Conclusion
AI accelerated structuring and draft generation but repeatedly filled information gaps with plausible features and accepted vague requirements. Human review was necessary to preserve evidence, define test oracles, control scope, and own the final baseline.

