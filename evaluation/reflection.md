
# Reflection

## What AI Did Well
AI helped organize the requirements engineering process into a structured workflow. It was useful for creating the first drafts of stakeholder analysis, elicitation findings, functional requirements, non-functional requirements, user stories, acceptance criteria, prioritization, validation, and change request analysis.

AI also helped maintain consistency across artifacts by using IDs such as `EL`, `FR`, `NFR`, `BR`, `US`, and `AC`.

## What AI Did Incorrectly
AI sometimes produced vague non-functional requirements such as "fast", "secure", and "reliable" without measurable criteria. AI also had a tendency to suggest useful but unsupported features, such as plagiarism detection or chat, even though those features were outside the current scope.

Another issue was that AI could write elicitation findings like final requirements too early. This required human correction so that elicitation remained focused on stakeholder evidence.

## Assumptions Found
- Authentication was assumed because the case mentioned security.
- Course enrollment was assumed because students should only see assignments for enrolled courses.
- Late submission policy was assumed to be configurable because the case mentioned deadlines but did not define the policy.

These assumptions were labeled explicitly so they would not be confused with confirmed facts.

## How SKILL.md Changes Improved Output
The skills improved the output because each `SKILL.md` defined:
- purpose
- when to use
- inputs
- required context
- workflow
- output format
- rules
- quality checks
- failure conditions
- example invocation
- expected output example

These sections made the AI output more systematic, reusable, and easier to review.

## Why Human Review Remains Necessary
Human review remains necessary because AI-generated requirements can look complete but still contain unsupported assumptions, vague wording, duplicated meaning, weak acceptance criteria, or missing traceability.

The student is responsible for deciding which requirements become part of the final baseline. AI can assist, but it cannot replace requirement validation and stakeholder judgment.

## How Traceability Helps
Traceability connects stakeholder needs, elicitation sources, requirements, user stories, acceptance criteria, and priorities. This helps detect unsupported requirements and makes change impact analysis easier.

For example, if a change request affects file submission, traceability helps identify related requirements, stories, acceptance criteria, and priorities.

## Final Reflection
AI is strongest when it is guided by clear reusable skills and reviewed by a human requirements engineer. The best result came from using AI for draft generation and then applying human review to improve clarity, testability, measurability, and traceability.
