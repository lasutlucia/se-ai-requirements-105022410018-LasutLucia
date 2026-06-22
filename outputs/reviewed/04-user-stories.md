
# 04 User Stories

## US-01: Create Assignment
As a lecturer, I want to create an assignment for a course, so that students know what task they must complete.

Related requirements: `FR-01`

Acceptance criteria:
- `AC-01`: Given an authenticated lecturer is assigned to a course, when the lecturer enters title, description, course, deadline, and submission instructions, then the assignment is saved and visible in the course.
- `AC-02`: Given required assignment fields are missing, when the lecturer submits the form, then the system rejects the form and shows field-level validation messages.

## US-02: Submit Assignment
As a student, I want to submit an assignment file, so that my lecturer can assess my work.

Related requirements: `FR-02`, `FR-09`

Acceptance criteria:
- `AC-03`: Given a student is enrolled in the course, when the student uploads an allowed file within the size limit, then the submission is saved with timestamp and status Submitted.
- `AC-04`: Given the uploaded file type or file size is not allowed, when the student submits the file, then the system rejects the upload and explains the reason.

## US-03: Track Assignment Status
As a student, I want to view assignment deadlines and submission status, so that I can manage my tasks.

Related requirements: `FR-03`, `FR-04`

Acceptance criteria:
- `AC-05`: Given a student opens the dashboard, when active assignments exist for enrolled courses, then the system displays each assignment deadline and current status.
- `AC-06`: Given a submission has been graded, when the student views the assignment, then the system displays status Graded with grade and feedback.

## US-04: Review Submission List
As a lecturer, I want to view submission lists, so that I can identify submitted, missing, and late work.

Related requirement: `FR-05`

Acceptance criteria:
- `AC-07`: Given a lecturer opens an assignment, when submissions exist, then the system displays student name, submission time, file link, status, grade, and feedback status.
- `AC-08`: Given an enrolled student has not submitted, when the lecturer opens the submission list, then the system displays Not Submitted for that student.

## US-05: Grade Submission
As a lecturer, I want to enter grades and written feedback, so that students receive assessment results.

Related requirement: `FR-06`

Acceptance criteria:
- `AC-09`: Given a submission exists, when the lecturer enters a valid grade and written feedback, then the system saves the grade and feedback.
- `AC-10`: Given the grade value is outside the allowed grade scale, when the lecturer saves, then the system rejects the value and shows an error message.

## US-06: Manage Users and Courses
As an administrator, I want to manage users, courses, and enrollments, so that assignment access follows campus data.

Related requirements: `FR-07`, `FR-08`

Acceptance criteria:
- `AC-11`: Given valid user data is entered, when the administrator saves the record, then the lecturer or student account is created or updated.
- `AC-12`: Given a student is enrolled in a course, when course assignments exist, then the student can view assignments for that course.

## US-07: Configure Assignment Rules
As an administrator, I want to configure file and late submission rules, so that submissions follow campus policy.

Related requirement: `FR-09`

Acceptance criteria:
- `AC-13`: Given an administrator sets accepted file types and maximum file size, when students upload files, then the system validates uploads against those settings.
- `AC-14`: Given late submission is disabled, when a student submits after the deadline, then the system rejects the submission.

## US-08: View Assignment Reports
As an administrator, I want assignment activity reports, so that I can monitor submission progress by course.

Related requirement: `FR-10`

Acceptance criteria:
- `AC-15`: Given assignment data exists, when the administrator opens a course report, then the system displays assignment count, submitted count, missing count, and late submission count.
- `AC-16`: Given no assignment exists for a course, when the report is opened, then the system displays zero counts instead of an error.

## Quality Check Result
Passed. There are at least six user stories and each user story has at least two testable acceptance criteria.
