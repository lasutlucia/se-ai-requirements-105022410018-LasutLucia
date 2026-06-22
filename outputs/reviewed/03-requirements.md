
# 03 Requirements

## Functional Requirements
| ID | Requirement | Stakeholder | Source |
|---|---|---|---|
| `FR-01` | The system shall allow lecturers to create assignments with title, description, course, deadline, and submission instructions. | Lecturer | `EL-01`, `EL-02` |
| `FR-02` | The system shall allow students to submit a file for an assignment according to accepted file type, maximum file size, and late submission policy. | Student | `EL-06`, `EL-11` |
| `FR-03` | The system shall display active assignments and deadlines to students for enrolled courses. | Student | `EL-05`, `ASSUMPTION A-07` |
| `FR-04` | The system shall display assignment status values to students: Not Submitted, Submitted, Late, Graded, and Returned. | Student | `EL-07`, `EL-08` |
| `FR-05` | The system shall allow lecturers to view a submission list per assignment, including student name, submission time, file link, status, grade, and feedback status. | Lecturer | `EL-03`, `INT-02` |
| `FR-06` | The system shall allow lecturers to open submitted files, enter grades, and provide written feedback. | Lecturer | `EL-04` |
| `FR-07` | The system shall allow administrators to create, update, deactivate, and view lecturer and student accounts. | Administrator | `EL-09` |
| `FR-08` | The system shall allow administrators to create, update, and view courses and enrollment relationships. | Administrator | `EL-10` |
| `FR-09` | The system shall allow administrators to configure accepted file types, maximum file size, and late submission policy. | Administrator | `EL-11`, `ASSUMPTION A-04` |
| `FR-10` | The system shall provide reports showing assignment count, submitted count, missing count, and late submission count by course. | Administrator | `EL-12` |

## Non-Functional Requirements
| ID | Requirement | Measurement / Test |
|---|---|---|
| `NFR-01` | The system shall require authenticated access before a user can view or modify assignment data. | 100% of protected pages redirect unauthenticated users to login. |
| `NFR-02` | The student assignment dashboard shall load within 3 seconds for 95% of requests under 100 concurrent users. | Performance test result shows response time threshold is met. |
| `NFR-03` | The system shall record create, update, submit, grade, and configuration actions in an audit log. | Audit log entry exists for each tested action. |
| `NFR-04` | The system shall maintain assignment, submission, grade, and feedback data without orphan records. | Database integrity test shows zero orphan records after create, update, and delete scenarios. |

## Business Rules
| ID | Rule | Source |
|---|---|---|
| `BR-01` | A student can submit only to assignments linked to courses where the student is enrolled. | `ASSUMPTION A-07` |
| `BR-02` | A lecturer can grade only assignments for courses assigned to that lecturer. | `ASSUMPTION A-06` |
| `BR-03` | If submission time is later than the deadline and late submission is allowed, the submission status shall be Late. | `EL-11`, `ASSUMPTION A-04` |

## Assumptions
- `ASSUMPTION A-02`: Users must authenticate before accessing assignment data.
- `ASSUMPTION A-04`: Late submission policy can be configured.
- `ASSUMPTION A-06`: Lecturers can only manage assignments for assigned courses.
- `ASSUMPTION A-07`: Students can only view and submit assignments for enrolled courses.

## Open Questions
- `OQ-02`: What exact file types and file size limits should be used?
- `OQ-04`: What grade scale should lecturers use?

## Quality Check Result
Passed. Functional requirements are traceable, non-functional requirements are measurable, and business rules are separated from system features.
