# Interview Guide Generator

Turns your organizational context and Engineering Competency Framework into structured, calibrated interview guides — so every hiring decision is grounded in who you are as a company and what you actually expect at each level.

Rather than generic question banks, this skill synthesizes your company's values, ways of working, and growth stage with the specific competencies defined for the role and level you're hiring. The result is an interview guide that reflects your standards, not someone else's template.

## Usage

```
/interview-guide-generator "Role: Senior UI Engineer. Project: e-commerce client, React/Next.js, 6-month engagement, small team, client-facing."
```

## What it does

- Extracts role and level from your prompt, loads the matching competency table from `shared/competencies/`
- Asks 2–3 clarifying questions to fill gaps (say "generate" to skip)
- Produces a full interview guide: role snapshot, interviewer notes, questions across 4 dimensions (Technical Craft, Delivery, Collaboration, Growth), red flags, scoring rubric, and candidate question decoder

## Requires

- **Company / organization context**: `shared/company.md` — organizational context that shapes what "good" looks like for any candidate. This file could describe:
  - **Organization type** — e.g. agency, startup, scale-up, enterprise. This affects what traits matter most (e.g. client-facing skills for agencies, ambiguity tolerance for early-stage startups).
  - **Company size** — headcount or team size, since it influences expectations around process, autonomy, and visibility.
  - **Growth stage** — early-stage, scaling, or established. Signals how much structure exists and how much initiative is expected.
  - **Core values** — the principles the organization explicitly holds (e.g. ownership, craft, honesty). These should anchor the "what good looks like" guidance in the guide.
  - **Ways of working** — e.g. async-first, cross-functional, feedback culture. Helps surface culture-fit signals during behavioral questions.
  - **What the environment rewards and is hard on** — concrete signals of fit and misfit for this specific context.
- **Role competency framework** — defines what's expected at each role and level, and anchors every question in the guide. This can be structured in different ways depending on how mature your organization's framework is:
  - **Single file** (`shared/competencies/engineering.md`) — all roles and levels in one document. Works well for smaller teams or early-stage frameworks.
  - **One file per role** (`shared/competencies/<role-slug>.md`) — e.g. `senior-ui-engineer.md`, `qa-analyst.md`. Recommended when roles have meaningfully different expectations.
  - **One file per level within a role** — e.g. `shared/competencies/ui-engineer/senior.md`. Useful when leveling distinctions are detailed and important to hiring calibration.
  - **External file** — a PDF, CSV, or spreadsheet you provide at invocation time. The skill will prompt you if it can't locate a matching file automatically.

  At minimum, each role entry should describe: core responsibilities, expected technical depth, delivery behaviors, and what distinguishes this level from the one below and above.
