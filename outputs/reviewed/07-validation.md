
# 07 Validation

## Validation Scope
Validated requirements: `FR-01`, `FR-02`, `FR-04`, `FR-06`, `FR-09`, `NFR-02`, and `NFR-04`.

## Validation Criteria
| Criterion | Meaning |
|---|---|
| Clarity | The requirement is understandable and avoids vague wording. |
| Completeness | The requirement has enough detail to be implemented and tested. |
| Consistency | The requirement does not conflict with other requirements. |
| Feasibility | The requirement can reasonably be implemented in the project context. |
| Testability | The requirement can be verified with pass or fail evidence. |
| Traceability | The requirement links to source, user story, acceptance criteria, and priority. |

## Validation Checklist
| Requirement ID | Clear | Complete | Consistent | Feasible | Testable | Traceable | Result |
|---|---|---|---|---|---|---|---|
| `FR-01` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-02` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-04` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-06` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `FR-09` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `NFR-02` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| `NFR-04` | Yes | Yes | Yes | Yes | Yes | Yes | Pass |

## Defects Found
| Requirement ID | Defect | Severity | Recommended Revision |
|---|---|---|---|
| Raw `NFR-02` | The raw output used vague wording such as "fast". | High | Replace with a measurable response time target. |
| Raw `NFR-04` | The raw output did not define how data integrity would be tested. | High | Add a zero orphan record database integrity test. |
| Raw `FR-02` | The first draft did not mention file type, file size, and late submission policy. | Medium | Link submission to administrator configuration rules. |

## Revised Requirements
| Requirement ID | Original Issue | Revised Requirement / Note |
|---|---|---|
| `FR-02` | Submission rule was incomplete. | Revised to include accepted file type, maximum file size, and late submission policy. |
| `NFR-02` | Performance was vague. | Revised to dashboard load within 3 seconds for 95% of requests under 100 concurrent users. |
| `NFR-04` | Data integrity was not testable. | Revised to require zero orphan records after tested workflows. |

## Minimum Content Check
- Functional requirements: Pass, 10 functional requirements exist.
- Non-functional requirements: Pass, 4 measurable non-functional requirements exist.
- Business rules: Pass, 3 business rules exist.
- User stories: Pass, 8 user stories exist.
- Acceptance criteria: Pass, each user story has at least 2 acceptance criteria.
- Prioritization: Pass, every functional requirement has MoSCoW priority.
- Validation: Pass, at least 5 requirements are validated.
- Change request: Pass, at least 1 change request has impact analysis and decision.

## Baseline Decision
The reviewed requirements baseline is acceptable for this assignment after revising vague non-functional requirements and confirming traceability.

## Quality Check Result
Passed. Validation covers clarity, completeness, consistency, feasibility, testability, and traceability.
