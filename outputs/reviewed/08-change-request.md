
# 08 Change Request

## Change Request
`CR-01`: Add plagiarism detection for submitted assignment files.

## Reason
Lecturers may want support for academic integrity checks when reviewing assignment submissions.

## Impact Analysis
| Area | Impact |
|---|---|
| Scope | Plagiarism detection is currently listed as out of scope in `CASE.md`. |
| Functional Requirements | Would require a new requirement for similarity checking after submission. |
| Non-Functional Requirements | Would require privacy, processing time, and data retention controls. |
| Business Rules | Would require rules about who can view similarity results and how results are used. |
| User Stories | Would add a lecturer user story for viewing plagiarism or similarity results. |
| Acceptance Criteria | Would require criteria for report generation, unavailable service handling, and result visibility. |
| Priority | Could be considered Should or Could in a future baseline, not Must for the current baseline. |
| Traceability | Requires new stakeholder approval or additional elicitation source before inclusion. |

## Affected Artifacts
| Artifact | Impact |
|---|---|
| `CASE.md` | Out-of-scope section would need revision if the request is approved. |
| `outputs/reviewed/03-requirements.md` | New FR and NFR entries would be required. |
| `outputs/reviewed/04-user-stories.md` | New user story and acceptance criteria would be required. |
| `outputs/reviewed/05-prioritization.md` | MoSCoW priority would need to be assigned. |
| `outputs/reviewed/requirements-traceability.md` | New traceability row would be required. |

## Decision
Defer.

## Decision Rationale
The change has potential value, but it is not part of the original assignment scope and would increase privacy, performance, validation, and traceability effort. It should be considered in a future version after the baseline assignment workflow is complete.

## Quality Check Result
Passed. The change request includes impact analysis, affected artifacts, and a justified decision.
