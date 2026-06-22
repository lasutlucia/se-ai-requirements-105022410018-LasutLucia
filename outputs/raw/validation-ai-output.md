
# Raw AI Output: Requirements Validation and Change Management

## Invocation
Read `CASE.md`, `outputs/reviewed/03-requirements.md`, `outputs/reviewed/04-user-stories.md`, `outputs/reviewed/05-prioritization.md`, and `outputs/reviewed/requirements-traceability.md`.
Execute `skills/05-validation-change/SKILL.md` exactly as written.
Validate at least five requirements.
Analyze this change request: "Add plagiarism detection for submitted assignment files."
Save raw AI output to `outputs/raw/validation-ai-output.md`.

## Validation Scope
Validated requirements: `FR-01`, `FR-02`, `FR-04`, `FR-06`, `FR-09`, `NFR-02`, and `NFR-04`.

## Validation Criteria
| Criterion | Meaning |
|---|---|
| Clarity | The requirement is understandable and avoids vague wording. |
| Completeness | The requirement has enough detail to be implemented and tested. |
| Consistency | The requirement does not conflict with other requirements. |
| Feasibility | The requirement can reasonably be implemented in the project context. |
| Testability | The requirement can be verified with pass/fail evidence. |
| Traceability | The requirement links to source, story, acceptance criteria, and priority. |

## Validation Checklist
| Requirement ID | Clear | Complete | Consistent | Feasible | Testable | Traceable | Result |
|---|---|---|---|---|---|---|---|
| `FR-01` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-02` | Yes | Partial | Yes | Yes | Yes | Yes | Needs review |
| `FR-04` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-06` | Yes | Partial | Yes | Yes | Yes | Yes | Needs review |
| `FR-09` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `NFR-02` | No | No | Yes | Yes | No | Partial | Needs revision |
| `NFR-04` | Partial | Partial | Yes | Yes | Partial | Partial | Needs revision |

## Defects Found
| Requirement ID | Defect | Severity | Recommended Revision |
|---|---|---|---|
| `FR-02` | File type, file size, and late submission behavior need clearer references to configuration. | Medium | Link the requirement to administrator configuration settings. |
| `FR-06` | Grade validity is not fully described. | Medium | Ensure acceptance criteria include invalid grade handling. |
| `NFR-02` | "Fast" is not measurable if used in raw draft. | High | Replace with a measurable response-time target. |
| `NFR-04` | Data integrity needs a concrete test. | High | Define zero orphan records after tested workflows. |

## Revised Requirements
| Requirement ID | Original Issue | Revised Requirement / Note |
|---|---|---|
| `NFR-02` | Ambiguous performance wording. | Dashboard should load within 3 seconds for 95% of requests under 100 concurrent users. |
| `NFR-04` | Data integrity not testable. | Database integrity test should show zero orphan assignment, submission, grade, or feedback records. |

## Minimum Content Check
- Functional requirements: Pass if at least 8 are included in reviewed output.
- Non-functional requirements: Needs review to ensure 4 are measurable.
- Business rules: Pass if at least 2 exist.
- User stories: Pass if at least 6 exist.
- Acceptance criteria: Pass if each user story has at least 2.
- Prioritization: Pass if all functional requirements have MoSCoW priority.
- Validation: Pass because at least 5 requirements are checked.

## Change Request
`CR-01`: Add plagiarism detection for submitted assignment files.

## Reason
Lecturers may want academic integrity support when reviewing submissions.

## Impact Analysis
| Area | Impact |
|---|---|
| Scope | Plagiarism detection is currently out of scope. |
| Functional Requirements | Would require a new requirement for similarity checking. |
| Non-Functional Requirements | Would require privacy, performance, and data retention rules. |
| User Stories | Would add a lecturer story for viewing similarity results. |
| Acceptance Criteria | Would require criteria for similarity report generation and failure handling. |
| Priority | Could be considered in a future baseline, not the current core workflow. |
| Traceability | Requires stakeholder approval or additional elicitation source. |

## Affected Artifacts
| Artifact | Impact |
|---|---|
| `CASE.md` | Out-of-scope list would need revision if approved. |
| `outputs/reviewed/03-requirements.md` | New FR and NFR would be needed. |
| `outputs/reviewed/04-user-stories.md` | New user story and acceptance criteria would be needed. |
| `outputs/reviewed/05-prioritization.md` | Priority would need to be assigned. |
| `outputs/reviewed/requirements-traceability.md` | New traceability row would be required. |

## Decision
Defer.

## Decision Rationale
The change has potential value but is outside the original scope and affects privacy, performance, validation effort, and traceability. It should be considered after the baseline assignment workflow is complete.

## Quality Check Result
Draft needs review. Validation found measurable wording issues in raw NFRs and the change request includes impact analysis.
