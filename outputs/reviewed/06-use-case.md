
# 06 Use Case

## Actors
- Lecturer
- Student
- Administrator

## Use Cases
| ID | Use Case | Actor | Related Requirements |
|---|---|---|---|
| `UC-01` | Create Assignment | Lecturer | `FR-01` |
| `UC-02` | Submit Assignment | Student | `FR-02` |
| `UC-03` | View Assignment Dashboard | Student | `FR-03`, `FR-04` |
| `UC-04` | Review Submission List | Lecturer | `FR-05` |
| `UC-05` | Grade and Give Feedback | Lecturer | `FR-06` |
| `UC-06` | Manage Users | Administrator | `FR-07` |
| `UC-07` | Manage Courses and Enrollments | Administrator | `FR-08` |
| `UC-08` | Configure Assignment Rules | Administrator | `FR-09` |
| `UC-09` | View Assignment Report | Administrator | `FR-10` |

## Main Scenario: Submit Assignment
1. Student logs in to the system.
2. Student opens the assignment dashboard.
3. System displays active assignments and deadlines for enrolled courses.
4. Student selects an assignment.
5. Student uploads an assignment file.
6. System validates file type and file size.
7. System checks deadline and late submission policy.
8. System saves the submission with timestamp and status.
9. System shows upload confirmation to the student.

## Alternative and Failure Scenarios
- If the file type is not allowed, the system rejects the upload and explains the reason.
- If the file size exceeds the maximum limit, the system rejects the upload and explains the reason.
- If late submission is disabled and the deadline has passed, the system rejects the submission.
- If late submission is enabled and the deadline has passed, the system saves the submission with status Late.
- If the student is not enrolled in the course, the assignment is not displayed to that student.

## Quality Check Result
Passed. The use case set includes at least three actors and more than six use cases.
