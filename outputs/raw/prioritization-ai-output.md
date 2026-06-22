
# Raw AI Output: Negotiation and Prioritization

## Invocation
Read `CASE.md`, `outputs/reviewed/01-inception.md`, `outputs/reviewed/02-elicitation.md`, `outputs/reviewed/03-requirements.md`, and `outputs/reviewed/04-user-stories.md`.
Execute `skills/04-prioritization/SKILL.md` exactly as written.
Save raw AI output to `outputs/raw/prioritization-ai-output.md`.

## Prioritization Criteria
| Priority | Meaning in This Project |
|---|---|
| Must | Required for the first usable assignment workflow or access control. |
| Should | Important for policy, monitoring, or quality but not required for the first baseline. |
| Could | Useful enhancement with lower immediate value. |
| Won't for now | Outside scope or intentionally deferred. |

## Prioritized Requirements
| Requirement ID | Requirement Summary | Stakeholder | Dependency | Priority | Reason |
|---|---|---|---|---|---|
| `FR-01` | Lecturer creates assignments. | Lecturer | None | Must | Assignments must exist before students can submit work. |
| `FR-02` | Student submits assignment files. | Student | `FR-01`, `FR-08`, `FR-09` | Must | Submission is the core student workflow. |
| `FR-03` | Student views active assignments and deadlines. | Student | `FR-01`, `FR-08` | Must | Students need assignment visibility to complete tasks. |
| `FR-04` | Student views assignment status. | Student | `FR-02`, `FR-06` | Must | Status tracking confirms submission and grading progress. |
| `FR-05` | Lecturer views submission list. | Lecturer | `FR-01`, `FR-02`, `FR-08` | Must | Lecturers need submission visibility before grading. |
| `FR-06` | Lecturer enters grades and feedback. | Lecturer | `FR-02`, `FR-05` | Must | Grading and feedback are required by the case. |
| `FR-07` | Administrator manages users. | Administrator | None | Must | User management controls system access. |
| `FR-08` | Administrator manages courses and enrollments. | Administrator | `FR-07` | Must | Course and enrollment data determine assignment access. |
| `FR-09` | Administrator configures file and late submission rules. | Administrator | `FR-02` | Should | Configuration improves policy control but can start with defaults. |
| `FR-10` | Administrator views assignment activity reports. | Administrator | `FR-01`, `FR-02`, `FR-08` | Should | Reports support monitoring but are not required for the first submission flow. |

## Dependencies
| Requirement | Depends On | Reason |
|---|---|---|
| `FR-02` | `FR-01`, `FR-08`, `FR-09` | Submission requires assignment, enrollment, and upload policy. |
| `FR-04` | `FR-02`, `FR-06` | Status depends on submission and grading events. |
| `FR-05` | `FR-01`, `FR-02`, `FR-08` | Submission list depends on assignment, submissions, and enrolled students. |
| `FR-10` | `FR-01`, `FR-02`, `FR-08` | Reports depend on assignment and submission data. |

## Stakeholder Conflicts
| Conflict ID | Stakeholders | Conflict | Proposed Resolution |
|---|---|---|---|
| `CF-01` | Lecturer, Administrator | Lecturers may want flexible late submission handling, while administrators need consistent policy control. | Use configurable late submission policy. |
| `CF-02` | Administrator, Lecturer | Administrators may want broad reports, while lecturers need grading workflow first. | Keep reports basic in the first baseline. |

## Trade-Off Decisions
| Decision ID | Trade-Off | Decision | Reason |
|---|---|---|---|
| `TD-01` | Flexible configuration vs faster baseline delivery. | Prioritize configuration as Should. | Core workflow can use default settings first. |
| `TD-02` | Complete reporting vs core submission workflow. | Prioritize reports as Should. | Submission and grading are more central to the case. |

## Deferred or Excluded Items
- Plagiarism detection.
- Real-time chat.
- Video conferencing.
- Payment features.

## Quality Check Result
Draft passed. All functional requirements have priorities and reasons. Human review should verify whether `FR-09` should be Must or Should.
