
# AI Output Review

## Purpose
This file records human review of AI-generated raw outputs. The raw AI outputs are stored in `outputs/raw/`, while corrected and validated outputs are stored in `outputs/reviewed/`.

## Review Summary
| Skill | Raw Output File | Reviewed Output File | Review Result |
|---|---|---|---|
| Project Inception | `outputs/raw/inception-ai-output.md` | `outputs/reviewed/01-inception.md` | Accepted with clearer scope and assumptions. |
| Requirements Elicitation | `outputs/raw/elicitation-ai-output.md` | `outputs/reviewed/02-elicitation.md` | Accepted with stronger source traceability. |
| Requirements Specification | `outputs/raw/requirements-ai-output.md` | `outputs/reviewed/03-requirements.md`, `outputs/reviewed/04-user-stories.md` | Revised because raw NFRs were vague. |
| Prioritization | `outputs/raw/prioritization-ai-output.md` | `outputs/reviewed/05-prioritization.md` | Accepted with clearer trade-off decisions. |
| Validation and Change | `outputs/raw/validation-ai-output.md` | `outputs/reviewed/07-validation.md`, `outputs/reviewed/08-change-request.md` | Accepted with clearer impact analysis. |

## Detailed Review: Requirements Elaboration and Specification

## Skill
Requirements Elaboration and Specification

## AI Output File
`outputs/raw/requirements-ai-output.md`

## Problems Found
1. AI used vague non-functional requirements such as "secure", "fast", "reliable", and "protect data integrity" without measurable tests.
2. `FR-02` initially allowed file submission but did not clearly mention accepted file type, maximum file size, and late submission policy.
3. Some acceptance criteria were too general, such as "system saves the submission" without describing validation and error conditions.
4. The raw output did not fully separate confirmed facts from assumptions.
5. Some requirements needed stronger links to elicitation IDs.

## Student Corrections
1. Changed vague performance wording into `NFR-02`: dashboard loads within 3 seconds for 95% of requests under 100 concurrent users.
2. Changed vague data integrity wording into `NFR-04`: database integrity test shows zero orphan records after tested workflows.
3. Revised `FR-02` so file submission follows file type, file size, and late submission policy.
4. Added clearer acceptance criteria for invalid file upload, invalid grade input, and zero-count reports.
5. Added traceability links in `outputs/reviewed/requirements-traceability.md`.

## Final Output
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/requirements-traceability.md`

## Why Human Review Was Necessary
AI produced useful structure quickly, but several outputs needed human correction to avoid vague wording, unsupported assumptions, and weak testability. Human review ensured that each requirement was measurable, traceable, and suitable for a final baseline.

## Quality Check Result
Passed. Problems, student corrections, and final output links are documented.
