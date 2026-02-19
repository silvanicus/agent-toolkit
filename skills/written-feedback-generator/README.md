# Written Feedback Generator

Structures written performance or peer feedback using the SBI model (Situation, Behavior, Impact).

## Usage

```
/written-feedback-generator "Name: Jamie. Role: Senior UI Engineer. Context: Lattice performance review. She delivers fast, high-quality work but is too quiet in team discussions."
```

## What it does

- Extracts the role and loads the matching competency table from `shared/competencies/`
- Analyzes strengths, areas for improvement, and competency gaps, then asks 2–4 clarifying questions (say "generate" to skip)
- Produces structured feedback: acknowledging opening, 2–4 SBI-formatted points, and a forward-looking close

## Requires

- `shared/competencies/<role-slug>.md` — competency framework for the target role (prompts you if missing)
