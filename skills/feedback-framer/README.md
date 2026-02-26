# Feedback Framer

Turns your observations and notes into structured, competency-anchored written feedback — so every review is consistent, fair, and grounded in what's actually expected at that role and level.

Rather than generic comments, this skill anchors your feedback in your organization's competency framework or role expectations, then structures it using the SBI model (Situation → Behavior → Impact). The result is feedback that reflects your standards and reads as credible and actionable.

## Usage

```
/feedback-framer "Name: Jamie. Role: Senior frontend engineer. Context: Lattice performance review. She delivers fast, high-quality work but is too quiet in team discussions."
```

## What it does

- Extracts the role and loads the matching competency table from your competency files (add the path or file name where your competency framework lives)
- Analyzes strengths, areas for improvement, and any competency gaps not covered in your notes
- Asks 2–4 clarifying questions to surface concrete examples and impact (say "generate" to skip)
- Produces structured feedback: an acknowledging opening, 2–4 SBI-formatted points, and a forward-looking close

## Requires

- **Role competency framework or role description** — required for the skill to anchor feedback in real expectations. Point to your competency file (add the path or file name here) or describe the role expectations inline when the skill asks.

- **Your notes or observations** — what you've seen, heard, or experienced. These don't need to be polished; the skill will help you structure and sharpen them.
