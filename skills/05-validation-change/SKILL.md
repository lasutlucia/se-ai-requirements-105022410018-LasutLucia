
# Requirements Validation and Change Management

## Purpose
This skill guides AI to validate the requirements baseline for the Student Task Management System and analyze requirement changes. It checks clarity, completeness, consistency, feasibility, testability, traceability, and change impact before requirements are accepted as a reviewed baseline.

The problem solved by this skill is preventing vague, inconsistent, untestable, or untraceable requirements from being accepted without human review.

## When to Use
Use this skill after requirements have been specified, user stories and acceptance criteria have been written, and prioritization has been completed.

Use it when:
- Requirements need to be validated before becoming a baseline.
- At least five requirements must be checked and revised if needed.
- Traceability must be verified.
- A change request must be analyzed.
- The project needs output for `outputs/reviewed/07-validation.md` and `outputs/reviewed/08-change-request.md`.

## Inputs
The following information must be available before this skill is executed:

- `CASE.md`
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/05-prioritization.md`
- `outputs/reviewed/requirements-traceability.md`
- A change request description.

## Required Context
AI must read the following files before producing output:

- `CASE.md`
- `outputs/reviewed/03-requirements.md`
- `outputs/reviewed/04-user-stories.md`
- `outputs/reviewed/05-prioritization.md`
- `outputs/reviewed/requirements-traceability.md`

AI must treat reviewed outputs as the current baseline candidate. AI must not approve a requirement or change request without checking its impact on related artifacts.

## Workflow
1. Read all required context files.
2. Select at least five requirements for validation.
3. Validate each selected requirement against clarity, completeness, consistency, feasibility, testability, and traceability.
4. Check whether each validated requirement links to stakeholder, source, user story, acceptance criteria, and priority.
5. Identify defects such as ambiguity, missing source, missing acceptance criteria, duplicated meaning, infeasible wording, or unmeasurable quality terms.
6. Recommend revisions only when the revision improves clarity, completeness, consistency, feasibility, testability, or traceability.
7. Preserve requirement IDs unless the requirement is removed or split.
8. Confirm that the requirements set satisfies the minimum content rules from the assignment:
   - At least 8 functional requirements.
   - At least 4 measurable non-functional requirements.
   - At least 2 business rules.
   - At least 6 user stories.
   - At least 2 acceptance criteria per user story.
   - All functional requirements have MoSCoW priority.
   - At least 5 requirements are validated.
   - At least 1 change request includes impact analysis and decision.
9. Analyze one change request.
10. Identify impacted functional requirements, non-functional requirements, business rules, user stories, acceptance criteria, priority, traceability, and scope.
11. Recommend one decision: Approve, Reject, or Defer.
12. Explain the decision with impact analysis.
13. Run the quality checks.
14. Stop and request clarification if traceability is missing or the change impact cannot be evaluated.

## Output Format
The output must be split into two reviewed artifacts:

### `outputs/reviewed/07-validation.md`
```md
# Requirements Validation Output

## Validation Scope

## Validation Criteria
| Criterion | Meaning |
|---|---|

## Validation Checklist
| Requirement ID | Clear | Complete | Consistent | Feasible | Testable | Traceable | Result |
|---|---|---|---|---|---|---|---|

## Defects Found
| Requirement ID | Defect | Severity | Recommended Revision |
|---|---|---|---|

## Revised Requirements
| Requirement ID | Original Issue | Revised Requirement / Note |
|---|---|---|

## Minimum Content Check

## Baseline Decision

## Quality Check Result
```

### `outputs/reviewed/08-change-request.md`
```md
# Change Request Output

## Change Request

## Reason

## Impact Analysis
| Area | Impact |
|---|---|

## Affected Artifacts
| Artifact | Impact |
|---|---|

## Decision

## Decision Rationale

## Quality Check Result
```

## Rules
- Validate at least five requirements.
- Do not accept vague requirements.
- Do not approve requirements without traceability.
- Do not revise requirements without explaining the reason.
- Do not change requirement IDs unless the requirement is split, merged, or removed.
- Every validation defect must be specific and actionable.
- Every change request must include impact analysis.
- Change decisions must be one of: Approve, Reject, or Defer.
- A change request that adds out-of-scope functionality must be marked Reject or Defer unless scope is intentionally changed.
- Do not invent stakeholder approval.
- Do not ignore affected user stories, acceptance criteria, priority, or traceability links.

## Quality Checks
Before finalizing the output, check that:

- At least five requirements are validated.
- Validation covers clarity, completeness, consistency, feasibility, testability, and traceability.
- Defects are clear and tied to specific requirements.
- Revisions improve the requirement rather than changing scope without reason.
- Minimum content rules from the assignment are checked.
- The change request includes impact analysis.
- Affected artifacts are listed.
- The decision is justified.
- The output can support the final requirements baseline.

## Failure Conditions
The skill must stop or request clarification if:

- `outputs/reviewed/03-requirements.md` is missing or empty.
- `outputs/reviewed/04-user-stories.md` is missing or empty.
- `outputs/reviewed/05-prioritization.md` is missing or empty.
- `outputs/reviewed/requirements-traceability.md` is missing or incomplete.
- Requirement IDs are missing.
- Acceptance criteria are missing for user stories.
- A change request is too vague to analyze.
- The impact of a change cannot be traced to affected artifacts.
- The AI must invent facts to approve or reject the change.

## Example Invocation
Read `CASE.md`, `outputs/reviewed/03-requirements.md`, `outputs/reviewed/04-user-stories.md`, `outputs/reviewed/05-prioritization.md`, and `outputs/reviewed/requirements-traceability.md`.

Execute `skills/05-validation-change/SKILL.md` exactly as written.

Validate at least five requirements.

Analyze this change request: "Add plagiarism detection for submitted assignment files."

Save raw AI output to `outputs/raw/validation-ai-output.md`.

After human review, save final validation output to `outputs/reviewed/07-validation.md` and final change request output to `outputs/reviewed/08-change-request.md`.

## Expected Output Example
```md
## Validation Checklist
| Requirement ID | Clear | Complete | Consistent | Feasible | Testable | Traceable | Result |
|---|---|---|---|---|---|---|---|
| FR-01 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| FR-02 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| NFR-02 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |
| FR-06 | Yes | Partial | Yes | Yes | Yes | Yes | Revised |
| FR-09 | Yes | Yes | Yes | Yes | Yes | Yes | Pass |

## Change Request Decision
Decision: Defer.

Reason: Plagiarism detection has value but is outside the current scope and affects submission processing, privacy, performance, reporting, and validation effort.
```
