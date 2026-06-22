
# 02 Elicitation

## Elicitation Objectives
- Understand lecturer workflow for assignment creation, submission monitoring, grading, and feedback.
- Understand student workflow for viewing assignments, submitting files, confirming uploads, and checking status.
- Understand administrator workflow for managing users, courses, enrollments, configuration, and reports.

## Elicitation Techniques
| Technique | Purpose | Stakeholder |
|---|---|---|
| Stakeholder Interview | Discover needs, pain points, and missing details. | Lecturer, Student, Administrator |
| Document Analysis | Extract facts from case, stakeholder notes, and assumptions. | All stakeholders |
| Scenario Analysis | Understand the assignment lifecycle from creation to reporting. | Lecturer, Student, Administrator |

## Interview Questions
### Lecturer
1. What information must be entered when creating an assignment?
2. How do you identify submitted, missing, and late submissions?
3. What information do you need before entering grades and feedback?

### Student
1. How do you know which assignments are active and due soon?
2. What confirmation do you need after uploading a file?
3. What assignment status information is useful after submission?

### Administrator
1. What user, course, and enrollment data must be managed?
2. What submission configuration settings are needed?
3. What reports are needed to monitor assignment activity?

## Elicitation Findings
| ID | Finding | Type | Stakeholder | Source | Rationale |
|---|---|---|---|---|---|
| `EL-01` | Lecturers need to create assignments for specific courses. | Explicit | Lecturer | `inputs/stakeholder-notes.md`, `INT-03` | Assignment creation is stated directly. |
| `EL-02` | Assignments need title, description, course, deadline, and submission instructions. | Explicit | Lecturer | `INT-03` | These fields are needed when creating assignments. |
| `EL-03` | Lecturers need to view submitted, missing, and late submissions. | Explicit | Lecturer | `INT-01`, `INT-02` | Lecturers need a submission list to reduce manual tracking errors. |
| `EL-04` | Lecturers need to open submitted files, enter grades, and write feedback. | Explicit | Lecturer | `INT-04` | Grading and feedback are part of assessment. |
| `EL-05` | Students need a dashboard showing active assignments and upcoming deadlines. | Explicit | Student | `INT-05` | Students need visibility of due work. |
| `EL-06` | Students need to upload assignment files. | Explicit | Student | `CASE.md`, `inputs/stakeholder-notes.md` | File submission is part of the case. |
| `EL-07` | Students need confirmation after file upload. | Explicit | Student | `INT-06` | Students need evidence that upload succeeded. |
| `EL-08` | Students need status values: Not Submitted, Submitted, Late, Graded, and Returned. | Explicit | Student | `INT-07` | Students requested clear status information. |
| `EL-09` | Administrators need to manage lecturer and student accounts. | Explicit | Administrator | `INT-09` | Account management is needed for access. |
| `EL-10` | Administrators need to manage courses and enrollments. | Explicit | Administrator | `INT-09` | Course and enrollment data controls assignment visibility. |
| `EL-11` | Administrators need to configure accepted file types, maximum file size, and late submission policy. | Explicit | Administrator | `INT-10` | Configuration settings are stated directly. |
| `EL-12` | Administrators need reports showing assignment count, submitted count, missing count, and late count by course. | Explicit | Administrator | `INT-11` | Reports are needed for monitoring. |
| `EL-13` | The system needs role-based access boundaries for lecturers, students, and administrators. | Implicit | All | `ASSUMPTION A-02`, `A-06`, `A-07` | Authentication and course ownership imply access boundaries. |

## Explicit Needs
- Assignment creation and deadline setting.
- Student file submission and upload confirmation.
- Submission status tracking.
- Lecturer grading and feedback.
- User, course, enrollment, and configuration management.
- Assignment activity reporting.

## Implicit Needs
- Consistent assignment status model.
- File validation based on administrator configuration.
- Role and enrollment based access control.

## Conflicts and Gaps
- Late submission behavior is not fully defined.
- File type and file size limits are not specified.
- Grade scale is not specified.
- Report filtering details are incomplete.

## Assumptions
- `ASSUMPTION A-02`: Users must authenticate before accessing assignment data.
- `ASSUMPTION A-06`: Lecturers can only manage assignments for assigned courses.
- `ASSUMPTION A-07`: Students can only view and submit assignments for enrolled courses.

## Open Questions
- `OQ-02`: What exact file types and file size limits should be allowed?
- `OQ-03`: Should late submissions be rejected or accepted with Late status?
- `OQ-04`: What grade scale should lecturers use?
- `OQ-05`: What report filters are required?

## Quality Check Result
Passed. All primary stakeholders are covered, findings have IDs, and explicit and implicit needs are separated.
