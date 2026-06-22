
# Examples for Requirements Validation and Change Management

## Example Invocation
```text
Read CASE.md, outputs/reviewed/03-requirements.md,
outputs/reviewed/04-user-stories.md, outputs/reviewed/05-prioritization.md,
and outputs/reviewed/requirements-traceability.md.

Execute skills/05-validation-change/SKILL.md exactly as written.
Validate at least five requirements.
Analyze this change request: Add plagiarism detection for submitted assignment files.
Save the first AI output to outputs/raw/validation-ai-output.md.
After review, save validation to outputs/reviewed/07-validation.md.
Save change request analysis to outputs/reviewed/08-change-request.md.
```

## Example Input Summary
Requirements available:

- `FR-01`: Lecturer creates assignments.
- `FR-02`: Student submits assignment files.
- `FR-04`: Student views assignment status.
- `FR-06`: Lecturer enters grades and feedback.
- `FR-09`: Administrator configures file and late submission rules.
- `NFR-02`: Dashboard loads within 3 seconds for 95% of requests under 100 concurrent users.
- `NFR-04`: System maintains data integrity without orphan records.

Change request:

- `CR-01`: Add plagiarism detection for submitted assignment files.

## Expected Output Example: Validation
```md
# Requirements Validation Output

## Validation Scope
Validated requirements: FR-01, FR-02, FR-04, FR-06, FR-09, NFR-02, and NFR-04.

## Validation Criteria
| Criterion | Meaning |
|---|---|
| Clarity | The requirement is easy to understand and has no vague wording. |
| Completeness | The requirement has enough detail to be implemented and tested. |
| Consistency | The requirement does not conflict with other requirements. |
| Feasibility | The requirement can reasonably be implemented in the project context. |
| Testability | The requirement has a pass or fail verification method. |
| Traceability | The requirement links to source, user story, acceptance criteria, and priority. |

## Validation Checklist
| Requirement ID | Clear | Complete | Consistent | Feasible | Testable | Traceable | Result |
|---|---|---|---|---|---|---|---|
| FR-01 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| FR-02 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| FR-04 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| FR-06 | Yes | Partial | Yes | Yes | Yes | Yes | Revised |
| FR-09 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| NFR-02 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| NFR-04 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |

## Defects Found
| Requirement ID | Defect | Severity | Recommended Revision |
|---|---|---|---|
| FR-06 | Grade validity is not fully explained in the requirement alone. | Medium | Ensure acceptance criteria define invalid grade handling. |
| Raw NFR wording | The first draft used vague words such as fast and reliable. | High | Replace with measurable performance and integrity tests. |

## Revised Requirements
| Requirement ID | Original Issue | Revised Requirement / Note |
|---|---|---|
| FR-06 | Grade validity needed clearer test support. | Keep FR-06 and validate it through AC-09 and AC-10. |
| NFR-02 | "Fast" was ambiguous. | Dashboard shall load within 3 seconds for 95% of requests under 100 concurrent users. |

## Minimum Content Check
- Functional requirements: Pass, at least 8 exist.
- Non-functional requirements: Pass, at least 4 measurable requirements exist.
- Business rules: Pass, at least 2 exist.
- User stories: Pass, at least 6 exist.
- Acceptance criteria: Pass, each user story has at least 2.
- Prioritization: Pass, functional requirements have MoSCoW priority.
- Validation: Pass, at least 5 requirements checked.

## Baseline Decision
The requirements baseline is acceptable after measurable wording and traceability checks are confirmed.

## Quality Check Result
Passed. Validation covers clarity, completeness, consistency, feasibility, testability, and traceability.
```

## Expected Output Example: Change Request
```md
# Change Request Output

## Change Request
CR-01: Add plagiarism detection for submitted assignment files.

## Reason
Lecturers may want support for academic integrity checks.

## Impact Analysis
| Area | Impact |
|---|---|
| Scope | Plagiarism detection is currently out of scope. |
| Functional Requirements | Would add a new requirement for similarity checking after submission. |
| Non-Functional Requirements | Would require privacy, processing time, and data retention controls. |
| User Stories | Would add a lecturer story for viewing similarity results. |
| Acceptance Criteria | Would require criteria for similarity report generation and failure handling. |
| Priority | Could be considered Should or Could in a future baseline, not Must for the current baseline. |
| Traceability | Requires new source evidence or stakeholder approval before inclusion. |

## Affected Artifacts
| Artifact | Impact |
|---|---|
| CASE.md | Out-of-scope section would need revision if approved. |
| outputs/reviewed/03-requirements.md | New FR and NFR entries would be required. |
| outputs/reviewed/04-user-stories.md | New user story and acceptance criteria would be required. |
| outputs/reviewed/05-prioritization.md | MoSCoW priority would need to be assigned. |
| outputs/reviewed/requirements-traceability.md | Traceability matrix would need new rows. |

## Decision
Defer.

## Decision Rationale
The change has potential value, but it is not part of the original assignment scope and increases privacy, performance, validation, and traceability effort. It should be considered in a future version after the baseline assignment workflow is complete.

## Quality Check Result
Passed. The change request includes impact analysis and a justified decision.
```

## Bad Output Example
```md
Approve plagiarism detection because it is useful.
```

## Why This Output Is Bad
- It does not analyze impact.
- It does not identify affected requirements or user stories.
- It ignores scope.
- It does not explain privacy, performance, or traceability consequences.
- It gives a decision without evidence.

## Good Practice Notes
- Validation is not just proofreading; it checks whether requirements can become a reliable baseline.
- A change request should not be accepted just because it is useful.
- Impact analysis must connect the change to requirements, stories, acceptance criteria, priority, and traceability.
- Human review remains necessary before final baseline approval.
