# Interview Guide Generator

Generates structured, role-calibrated interview guides for hiring across engineering levels.

## Usage

```
/interview-guide-generator "Role: Senior UI Engineer. Project: e-commerce client, React/Next.js, 6-month engagement, small team, client-facing."
```

## What it does

- Extracts role and level from your prompt, loads the matching competency table from `shared/competencies/`
- Asks 2–3 clarifying questions to fill gaps (say "generate" to skip)
- Produces a full interview guide: role snapshot, interviewer notes, questions across 4 dimensions (Technical Craft, Delivery, Collaboration, Growth), red flags, scoring rubric, and candidate question decoder

## Requires

- `shared/company.md` — organizational context
- `shared/competencies/<role-slug>.md` — competency framework for the target role (prompts you if missing)
