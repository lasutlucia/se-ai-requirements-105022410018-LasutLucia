
# Raw AI Output: Project Inception

## Invocation
Read `CASE.md`, `inputs/stakeholder-notes.md`, and `inputs/assumptions.md`.
Execute `skills/01-inception/SKILL.md` exactly as written.
Save the result using the output structure defined in the skill.
Do not invent missing facts. Mark assumptions and open questions explicitly.

## Business Problem
Lecturers, students, and administrators need a more organized way to manage course assignments, assignment submissions, grading, deadlines, feedback, and reporting. Without a centralized workflow, assignment information can be spread across different tools and become difficult to monitor.

The problem is not only file upload. The broader business problem is maintaining accurate and traceable assignment information from assignment creation until submission, grading, feedback, and reporting.

## Business Goals
- Centralize assignment management for lecturers, students, and administrators.
- Improve visibility of assignment deadlines and submission status.
- Help lecturers monitor submitted, missing, late, graded, and returned assignments.
- Help administrators manage users, courses, enrollments, configuration, and reporting.
- Improve data integrity for assignment, submission, grade, and feedback records.

## Stakeholders
| Stakeholder | Type | Needs | Source |
|---|---|---|---|
| Lecturer | Primary | Create assignments, set deadlines, view submissions, enter grades, and provide feedback. | `CASE.md`, `stakeholder-notes.md` |
| Student | Primary | View assignments, submit files, receive confirmation, monitor status, and view grades and feedback. | `CASE.md`, `stakeholder-notes.md` |
| Administrator | Primary | Manage users, courses, enrollments, configuration, and reports. | `CASE.md`, `stakeholder-notes.md` |

## Scope
### In Scope
- Assignment creation.
- Deadline management.
- Student file submission.
- Submission confirmation and status tracking.
- Grading and feedback.
- User management.
- Course and enrollment management.
- Assignment configuration.
- Basic assignment activity reporting.

### Out of Scope
- Plagiarism detection.
- Real-time chat.
- Video conferencing.
- Payment features.
- Academic transcript management.

## Assumptions
- `ASSUMPTION A-01`: The campus already has lecturer, student, course, and enrollment data.
- `ASSUMPTION A-02`: Users must authenticate before accessing assignment data.
- `ASSUMPTION A-03`: Student submission files are stored by the system and linked to the correct assignment and student.
- `ASSUMPTION A-04`: Late submission policy can be configured by an administrator.

## Constraints
- The system must consider usability, security, performance, reliability, and data integrity.
- Requirements must be testable and traceable.
- Unsupported assumptions must be labeled.

## Open Questions
- `OPEN QUESTION`: What authentication method should be used?
- `OPEN QUESTION`: What file types and maximum file size should be allowed?
- `OPEN QUESTION`: Should late submissions be blocked or accepted with a Late status?
- `OPEN QUESTION`: What exact report filters are required?

## Quality Check Result
Draft passed. Stakeholders, goals, scope, assumptions, constraints, and open questions are separated. Further review is still needed to confirm assumptions and boundaries.
