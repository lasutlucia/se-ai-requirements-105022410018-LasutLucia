
# Raw AI Output: Requirements Elicitation

## Invocation
Read `CASE.md`, `outputs/reviewed/01-inception.md`, `inputs/stakeholder-notes.md`, `inputs/interview-answers.md`, and `inputs/assumptions.md`.
Execute `skills/02-elicitation/SKILL.md` exactly as written.
Save the result to `outputs/raw/elicitation-ai-output.md`.

## Elicitation Objectives
- Understand how lecturers create assignments, monitor submissions, grade work, and give feedback.
- Understand how students view assignments, submit files, confirm uploads, and track status.
- Understand how administrators manage users, courses, enrollments, configuration, and reports.

## Elicitation Techniques
| Technique | Purpose | Stakeholder |
|---|---|---|
| Stakeholder Interview | Discover goals, pain points, and missing details. | Lecturer, Student, Administrator |
| Document Analysis | Extract known facts from the case and stakeholder notes. | All stakeholders |
| Scenario Analysis | Understand the assignment workflow from creation to grading. | Lecturer, Student |

## Interview Questions
### Lecturer
1. What information must be entered when creating an assignment?
2. How do you track submitted, missing, and late submissions?
3. What information is needed before entering grades and feedback?

### Student
1. How do you know which assignments are due soon?
2. What confirmation do you need after submitting a file?
3. What status information do you need after submission?

### Administrator
1. What user and course data must be managed?
2. What assignment configuration settings are needed?
3. What reports are needed for assignment monitoring?

## Elicitation Findings
| ID | Finding | Type | Stakeholder | Source | Rationale |
|---|---|---|---|---|---|
| `EL-01` | Lecturers need to create assignments for specific courses. | Explicit | Lecturer | `stakeholder-notes.md`, `INT-03` | Assignment creation is repeatedly stated. |
| `EL-02` | Assignments need title, description, course, deadline, and submission instructions. | Explicit | Lecturer | `INT-03` | Lecturer needs these fields when creating assignments. |
| `EL-03` | Lecturers need to view submitted, missing, and late submissions. | Explicit | Lecturer | `INT-01`, `INT-02` | Manual tracking is difficult without a clear list. |
| `EL-04` | Lecturers need to enter grades and written feedback. | Explicit | Lecturer | `INT-04` | Grading and feedback are part of assessment. |
| `EL-05` | Students need a dashboard for active assignments and deadlines. | Explicit | Student | `INT-05` | Students need deadline visibility. |
| `EL-06` | Students need to upload assignment files. | Explicit | Student | `CASE.md`, `stakeholder-notes.md` | File submission is part of the case. |
| `EL-07` | Students need confirmation after file upload. | Explicit | Student | `INT-06` | Students want to know the upload succeeded. |
| `EL-08` | Students need status values such as Not Submitted, Submitted, Late, Graded, and Returned. | Explicit | Student | `INT-07` | Students requested these statuses. |
| `EL-09` | Administrators need to manage lecturer and student accounts. | Explicit | Administrator | `INT-09` | Account management is needed for access. |
| `EL-10` | Administrators need to manage courses and enrollments. | Explicit | Administrator | `INT-09` | Course and enrollment data determine assignment access. |
| `EL-11` | Administrators need accepted file type, maximum file size, and late submission settings. | Explicit | Administrator | `INT-10` | Configuration settings were stated directly. |
| `EL-12` | Administrators need assignment activity reports by course. | Explicit | Administrator | `INT-11` | Reports are needed for monitoring. |

## Explicit Needs
- Assignment creation and deadline setting.
- File submission and submission confirmation.
- Submission status tracking.
- Grading and feedback.
- User, course, enrollment, and configuration management.
- Basic assignment activity reporting.

## Implicit Needs
- The system needs a consistent submission status model.
- The system needs validation rules for file type and size.
- The system needs access control based on user role and course enrollment.

## Conflicts and Gaps
- Late submission policy is not fully defined.
- Accepted file types and maximum file size are not specified.
- Grade scale is not specified.
- Report filters beyond course-level counts are unclear.

## Assumptions
- `ASSUMPTION A-02`: Users must authenticate before accessing assignment data.
- `ASSUMPTION A-06`: Lecturers can only manage assignments for assigned courses.
- `ASSUMPTION A-07`: Students can only view and submit assignments for enrolled courses.

## Open Questions
- `OPEN QUESTION`: What exact file types and file size limits are allowed?
- `OPEN QUESTION`: What grade scale should lecturers use?
- `OPEN QUESTION`: Should late submissions be rejected or accepted with a Late status?

## Quality Check Result
Draft passed. All primary stakeholders are covered and findings have IDs. Human review is needed to confirm whether implicit needs are acceptable.
