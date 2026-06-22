
# 01 Inception

## Business Problem
Lecturers, students, and administrators need a consistent way to manage assignment information from assignment creation until grading and reporting. Without a centralized workflow, assignment status, deadlines, submissions, grades, and feedback can become difficult to monitor, verify, and trace.

The business problem is not only file upload. The broader problem is maintaining accurate, timely, and traceable assignment information for every stakeholder involved in the academic assignment process.

## Business Goals
- Centralize assignment creation, submission, grading, feedback, and reporting.
- Improve student visibility of active assignments, deadlines, submission confirmation, and grades.
- Help lecturers monitor submitted, missing, late, graded, and returned assignments.
- Help administrators maintain consistent user, course, enrollment, configuration, and reporting data.
- Ensure assignment records support usability, security, performance, reliability, and data integrity.

## Stakeholders
| Stakeholder | Type | Needs | Source |
|---|---|---|---|
| Lecturer | Primary | Create assignments, set deadlines, monitor submissions, grade work, and provide feedback. | `CASE.md`, `inputs/stakeholder-notes.md` |
| Student | Primary | View assignments, submit files, receive upload confirmation, track status, and view grades and feedback. | `CASE.md`, `inputs/stakeholder-notes.md` |
| Administrator | Primary | Manage users, courses, enrollments, configuration, and assignment activity reports. | `CASE.md`, `inputs/stakeholder-notes.md` |
| Course Management Office | Secondary | Use reliable assignment activity information for monitoring. | `CASE.md` |

## Scope
### In Scope
- Assignment creation and deadline management.
- Student file submission.
- Submission confirmation and status tracking.
- Lecturer grading and written feedback.
- User account management.
- Course and enrollment management.
- Assignment configuration for file type, file size, and late submission policy.
- Basic assignment and submission activity reporting.

### Out of Scope
- Plagiarism detection.
- Real-time chat.
- Video conferencing.
- Payment or financial features.
- Full learning material management.
- Academic transcript management.

## Assumptions
- `ASSUMPTION A-01`: The campus already has lecturer, student, course, and enrollment data.
- `ASSUMPTION A-02`: Users must authenticate before accessing assignment data.
- `ASSUMPTION A-03`: Student submission files are stored by the system and linked to assignment, student, course, and timestamp.
- `ASSUMPTION A-04`: Late submission policy can be configured by an administrator.
- `ASSUMPTION A-05`: Reporting is limited to assignment and submission activity, not academic transcript reporting.

## Constraints
- Requirements must be testable and traceable.
- Unsupported assumptions must be labeled explicitly.
- The system must consider usability, security, performance, reliability, and data integrity.
- AI-generated output must be reviewed before becoming final output.

## Open Questions
- `OQ-01`: What authentication method should be used?
- `OQ-02`: What file types and maximum file size should be accepted?
- `OQ-03`: Should late submissions be blocked, accepted with Late status, or configured per course?
- `OQ-04`: What grade scale should lecturers use?
- `OQ-05`: What report filters are required by lecturers and administrators?

## Quality Check Result
Passed. The reviewed inception output separates business problem, goals, stakeholders, scope, assumptions, constraints, and open questions.
