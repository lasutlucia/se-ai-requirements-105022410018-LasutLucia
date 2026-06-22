
# 05 Prioritization

## Prioritization Criteria
| Priority | Meaning in This Project |
|---|---|
| Must | Required for the first usable assignment workflow or access control. |
| Should | Important for policy control or monitoring but can be delayed after the first baseline. |
| Could | Useful enhancement with lower immediate value. |
| Won't for now | Outside scope or intentionally deferred. |

## Prioritized Requirements
| Requirement ID | Requirement Summary | Stakeholder | Dependency | Priority | Reason |
|---|---|---|---|---|---|
| `FR-01` | Lecturer creates assignments. | Lecturer | None | Must | Assignments must exist before students can submit work. |
| `FR-02` | Student submits assignment files. | Student | `FR-01`, `FR-08`, `FR-09` | Must | File submission is the core student workflow. |
| `FR-03` | Student views active assignments and deadlines. | Student | `FR-01`, `FR-08` | Must | Students need assignment visibility to complete tasks. |
| `FR-04` | Student views assignment status. | Student | `FR-02`, `FR-06` | Must | Status tracking confirms submission and grading progress. |
| `FR-05` | Lecturer views submission list. | Lecturer | `FR-01`, `FR-02`, `FR-08` | Must | Lecturers need submission visibility before grading. |
| `FR-06` | Lecturer enters grades and feedback. | Lecturer | `FR-02`, `FR-05` | Must | Grading and feedback are required by the case. |
| `FR-07` | Administrator manages users. | Administrator | None | Must | User management controls access to the system. |
| `FR-08` | Administrator manages courses and enrollments. | Administrator | `FR-07` | Must | Course and enrollment data determine assignment access. |
| `FR-09` | Administrator configures file and late submission rules. | Administrator | `FR-02` | Should | Configuration improves policy control but the first baseline can use default settings. |
| `FR-10` | Administrator views assignment activity reports. | Administrator | `FR-01`, `FR-02`, `FR-08` | Should | Reports support monitoring but are not required for the first submission and grading workflow. |

## Dependencies
| Requirement | Depends On | Reason |
|---|---|---|
| `FR-02` | `FR-01`, `FR-08`, `FR-09` | A student can submit only when assignment, enrollment, and upload policy exist. |
| `FR-04` | `FR-02`, `FR-06` | Status depends on submission and grading events. |
| `FR-05` | `FR-01`, `FR-02`, `FR-08` | Lecturer submission list depends on assignments, submissions, and enrollment. |
| `FR-10` | `FR-01`, `FR-02`, `FR-08` | Reports depend on assignment and submission data. |

## Stakeholder Conflicts
| Conflict ID | Stakeholders | Conflict | Proposed Resolution |
|---|---|---|---|
| `CF-01` | Lecturer, Administrator | Lecturers may want flexible late submission handling, while administrators need consistent policy control. | Use configurable late submission policy and prioritize configuration as Should. |
| `CF-02` | Administrator, Lecturer | Administrators may want broad reports, while lecturers need the grading workflow first. | Limit first report scope to assignment and submission counts. |

## Trade-Off Decisions
| Decision ID | Trade-Off | Decision | Reason |
|---|---|---|---|
| `TD-01` | Flexible configuration vs faster baseline delivery. | Prioritize `FR-09` as Should. | The core workflow can start with default submission settings. |
| `TD-02` | Complete reporting vs core submission workflow. | Prioritize `FR-10` as Should. | Reporting is useful but less critical than creation, submission, and grading. |

## Deferred or Excluded Items
- Plagiarism detection remains out of scope.
- Real-time chat remains out of scope.
- Video conferencing remains out of scope.

## Quality Check Result
Passed. Every functional requirement has MoSCoW priority, dependency analysis, and a decision reason.
