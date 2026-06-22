
# Raw AI Output: Requirements Elaboration and Specification

## Invocation
Read `CASE.md`, `outputs/reviewed/01-inception.md`, `outputs/reviewed/02-elicitation.md`, and `inputs/assumptions.md`.
Execute `skills/03-specification/SKILL.md` exactly as written.
Save raw AI output to `outputs/raw/requirements-ai-output.md`.

## Functional Requirements
| ID | Requirement | Stakeholder | Source |
|---|---|---|---|
| `FR-01` | The system shall allow lecturers to create assignments with title, description, course, deadline, and submission instructions. | Lecturer | `EL-01`, `EL-02` |
| `FR-02` | The system shall allow students to submit assignment files. | Student | `EL-06` |
| `FR-03` | The system shall display active assignments and deadlines to students. | Student | `EL-05` |
| `FR-04` | The system shall show submission status values to students. | Student | `EL-07`, `EL-08` |
| `FR-05` | The system shall allow lecturers to view submission lists per assignment. | Lecturer | `EL-03` |
| `FR-06` | The system shall allow lecturers to enter grades and feedback for submitted assignments. | Lecturer | `EL-04` |
| `FR-07` | The system shall allow administrators to manage lecturer and student accounts. | Administrator | `EL-09` |
| `FR-08` | The system shall allow administrators to manage courses and enrollments. | Administrator | `EL-10` |
| `FR-09` | The system shall allow administrators to configure accepted file types, maximum file size, and late submission policy. | Administrator | `EL-11` |
| `FR-10` | The system shall provide reports about assignment and submission activity by course. | Administrator | `EL-12` |

## Non-Functional Requirements
| ID | Requirement | Measurement / Test |
|---|---|---|
| `NFR-01` | The system must be secure. | Needs review because "secure" is broad. |
| `NFR-02` | The system must be fast. | Needs review because "fast" is not measurable. |
| `NFR-03` | The system must be reliable. | Needs review because "reliable" is not measurable yet. |
| `NFR-04` | The system must protect data integrity. | Needs review and measurable test. |

## Business Rules
| ID | Rule | Source |
|---|---|---|
| `BR-01` | A student can submit only to assignments for courses where the student is enrolled. | `ASSUMPTION A-07` |
| `BR-02` | A lecturer can grade only assignments for courses assigned to that lecturer. | `ASSUMPTION A-06` |
| `BR-03` | If a submission is uploaded after deadline and late submission is allowed, status should be Late. | `EL-11`, `ASSUMPTION A-04` |

## User Stories
### `US-01`: Create Assignment
As a lecturer, I want to create an assignment for a course, so that students know what task they must complete.

Related requirements: `FR-01`

Acceptance criteria:
- `AC-01`: Given a lecturer enters complete assignment data, when the lecturer submits the form, then the system saves the assignment.
- `AC-02`: Given required fields are missing, when the lecturer submits the form, then the system rejects the form.

### `US-02`: Submit Assignment
As a student, I want to submit an assignment file, so that my lecturer can assess my work.

Related requirements: `FR-02`

Acceptance criteria:
- `AC-03`: Given the file is valid, when the student uploads the file, then the system saves the submission.
- `AC-04`: Given the file is invalid, when the student uploads the file, then the system rejects the submission.

### `US-03`: Track Assignment Status
As a student, I want to view assignment status and deadlines, so that I can manage my tasks.

Related requirements: `FR-03`, `FR-04`

Acceptance criteria:
- `AC-05`: Given active assignments exist, when the student opens the dashboard, then the system displays deadlines and status.
- `AC-06`: Given a submission has been graded, when the student views the assignment, then the system shows status Graded.

### `US-04`: Review Submissions
As a lecturer, I want to view submission lists, so that I can identify submitted and missing work.

Related requirement: `FR-05`

Acceptance criteria:
- `AC-07`: Given submissions exist, when the lecturer opens the assignment, then the system displays the submission list.
- `AC-08`: Given no submission exists for a student, when the list is opened, then the system displays Not Submitted.

### `US-05`: Grade Submission
As a lecturer, I want to enter grades and feedback, so that students receive assessment results.

Related requirement: `FR-06`

Acceptance criteria:
- `AC-09`: Given a submission exists, when the lecturer enters a grade and feedback, then the system saves them.
- `AC-10`: Given invalid grade input, when the lecturer saves, then the system rejects the value.

### `US-06`: Manage Users and Courses
As an administrator, I want to manage users, courses, and enrollments, so that assignment access is correct.

Related requirements: `FR-07`, `FR-08`

Acceptance criteria:
- `AC-11`: Given valid user data, when the administrator saves it, then the user record is created or updated.
- `AC-12`: Given a student is enrolled in a course, when course assignments exist, then the student can view those assignments.

## Assumptions
- `ASSUMPTION A-02`: Authentication is required.
- `ASSUMPTION A-04`: Late submission policy can be configured.

## Open Questions
- `OPEN QUESTION`: What grade scale is used?
- `OPEN QUESTION`: What exact file size limit should be configured?

## Quality Check Result
Draft needs review. Functional requirements are traceable, but non-functional requirements still contain vague terms and must be revised in the reviewed output.
