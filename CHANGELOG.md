
# Changelog

All notable changes for the AI-Assisted Requirements Engineering assignment are documented in this file.

## 2026-06-22

### Added
- Added `README.md` with student information, project overview, skill links, final output links, AI usage, and reflection summary.
- Added `CASE.md` for the Student Task Management System case context, including business problem, goals, stakeholders, scope, assumptions, constraints, and open questions.
- Added five reusable AI skills:
  - `skills/01-inception/SKILL.md`
  - `skills/02-elicitation/SKILL.md`
  - `skills/03-specification/SKILL.md`
  - `skills/04-prioritization/SKILL.md`
  - `skills/05-validation-change/SKILL.md`
- Added examples for each skill in `examples.md`.
- Added input files:
  - `inputs/stakeholder-notes.md`
  - `inputs/interview-answers.md`
  - `inputs/assumptions.md`
- Added raw AI output files:
  - `outputs/raw/inception-ai-output.md`
  - `outputs/raw/elicitation-ai-output.md`
  - `outputs/raw/requirements-ai-output.md`
  - `outputs/raw/prioritization-ai-output.md`
  - `outputs/raw/validation-ai-output.md`
- Added reviewed output files:
  - `outputs/reviewed/01-inception.md`
  - `outputs/reviewed/02-elicitation.md`
  - `outputs/reviewed/03-requirements.md`
  - `outputs/reviewed/04-user-stories.md`
  - `outputs/reviewed/05-prioritization.md`
  - `outputs/reviewed/06-use-case.md`
  - `outputs/reviewed/07-validation.md`
  - `outputs/reviewed/08-change-request.md`
  - `outputs/reviewed/requirements-traceability.md`
- Added use case diagram files:
  - `diagrams/use-case-diagram.png`
  - `diagrams/use-case-diagram.drawio`
- Added evaluation files:
  - `evaluation/ai-output-review.md`
  - `evaluation/skill-test-results.md`
  - `evaluation/reflection.md`

### Changed
- Renamed skill example files from `exemples.md` to `examples.md` to match the assignment structure.
- Revised raw AI outputs into reviewed outputs with clearer traceability and measurable requirements.
- Replaced vague non-functional requirement wording such as "fast", "secure", and "reliable" with measurable criteria in reviewed requirements.
- Added explicit requirement IDs, user story IDs, acceptance criteria IDs, and source references.
- Added MoSCoW prioritization and trade-off explanations for all functional requirements.
- Added validation results covering clarity, completeness, consistency, feasibility, testability, and traceability.
- Added change request impact analysis for plagiarism detection and deferred it as a future enhancement.

### Skill Testing Notes
- Tested the Project Inception skill using a Clinic Appointment System case.
- Tested the Requirements Elicitation skill using a Library Reservation System case.
- Identified that AI may add unsupported assumptions such as notification channels.
- Improved the skill usage by enforcing rules against unsupported assumptions and premature requirements.

### Review Notes
- Raw AI outputs were preserved in `outputs/raw/`.
- Reviewed and corrected outputs were saved in `outputs/reviewed/`.
- Human review corrected vague NFRs, missing source links, and weak acceptance criteria.
- Traceability matrix was added to connect requirements, stakeholders, sources, user stories, acceptance criteria, and priority.

### Repository Status
- Repository structure follows the assignment requirement.
- Five skills are available and reusable.
- Raw and reviewed outputs are available.
- Use case diagram is available in PNG and Draw.io formats.
- Evaluation and reflection files are available.
