
# Assumptions

## Purpose
This file records assumptions used during requirements engineering for the Student Task Management System. Each assumption must be reviewed and should not be treated as a confirmed fact unless validated by a stakeholder.

## Assumption List

### ASSUMPTION A-01
The campus already has lecturer, student, course, and enrollment data that can be used by the system.

**Reason:** The case states that administrators manage users and courses, but it does not explain whether the data already exists.

### ASSUMPTION A-02
Users must authenticate before accessing assignment data.

**Reason:** The case mentions security, and assignment data should not be publicly accessible.

### ASSUMPTION A-03
Student submission files are stored by the system and linked to the correct assignment, student, course, and timestamp.

**Reason:** The case requires file submission and submission status tracking.

### ASSUMPTION A-04
Late submission policy can be configured by an administrator.

**Reason:** The case mentions deadlines, but it does not define whether late submissions are accepted or rejected.

### ASSUMPTION A-05
Reports are limited to assignment and submission activity, not academic transcript reporting.

**Reason:** The case mentions reporting in the context of assignment management only.

### ASSUMPTION A-06
Lecturers can only manage assignments for courses assigned to them.

**Reason:** This protects course ownership and supports data integrity.

### ASSUMPTION A-07
Students can only view and submit assignments for courses where they are enrolled.

**Reason:** This supports access control and correct assignment visibility.

## Open Assumption Questions
- `OPEN QUESTION`: What authentication method should be used?
- `OPEN QUESTION`: What exact file types and maximum file size are allowed?
- `OPEN QUESTION`: What grade scale should lecturers use?
- `OPEN QUESTION`: Should late submissions be blocked or accepted with a Late status?

## Notes for AI Use
- Any output that uses these assumptions must keep the `ASSUMPTION` label.
- Assumptions must be reviewed before becoming final baseline requirements.
- If an assumption affects scope or priority, it must be mentioned in the related output file.
