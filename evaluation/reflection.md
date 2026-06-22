# Reflection

## What did AI do well?
AI was effective at rapidly proposing document structure, identifying common stakeholder perspectives, converting repeated information into tables, and generating candidate scenarios. It also helped expose where a requirement needed a success path, failure path, source, or verification method. This reduced mechanical drafting effort and made cross-document comparison faster.

## What errors or assumptions did AI make most often?
The most common error was completing missing context with plausible product conventions. Examples included chat, email notification, plagiarism detection, mobile applications, AWS, SSO, and delivery dates. AI also preferred attractive but untestable words such as “fast”, “secure”, and “user-friendly”. These outputs sounded reasonable while lacking evidence or a test oracle.

## How did SKILL.md changes improve output quality?
The revised skills require source IDs, stable artefact IDs, explicit assumptions, open-question owners, measurable NFR fields, failure conditions, and cross-artefact quality gates. Those constraints changed missing information from an invitation to guess into a visible reason to stop or request clarification. Testing on clinic and library cases demonstrated that the controls transfer beyond the assignment case.

## Why is human review still necessary?
A workflow can improve consistency but cannot grant AI authority to decide academic policy, privacy, budgets, risk tolerance, or stakeholder trade-offs. Human review verifies whether evidence is genuine, whether assumed targets are acceptable, and whether a change should enter the baseline. The final requirement baseline is therefore a human decision supported—not replaced—by AI.

## How does traceability preserve consistency?
Traceability makes every requirement answerable to a stakeholder and source, then connects it to stories, acceptance criteria, use cases, and priority. When a requirement changes, the matrix reveals the downstream artefacts that must be reviewed. It also exposes orphan features, missing tests, inconsistent IDs, and unsupported priorities before they become design or implementation defects.

