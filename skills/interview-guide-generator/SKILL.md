---
name: interview-guide-generator
description: Generates structured, role-calibrated interview guides for hiring across engineering levels. Use when preparing to interview a candidate for a specific role and context.
---

# Overview
This skill generates a tailored, structured interview guide for a specific role and hiring context.
It anchors every question to the competency framework for that level, incorporates project-specific
technical requirements when provided, and produces a guide that any interviewer on the team can pick
up and run with consistently.

The goal is to remove subjectivity from the interview process, ensure signal collection is calibrated
to what actually matters at that level, and make the hiring bar consistent across directors and leads.

---

# When to Use This Skill
- Opening a new position and preparing the interview loop.
- Hiring for a project with specific technical, domain, or client requirements.
- Calibrating a hiring panel that includes people who don't interview frequently.
- Creating a repeatable guide for a role you hire for often (e.g., M3 Senior UI Engineer).
- Refreshing an outdated interview process for an existing role.

# When NOT to Use This Skill
- For contractor or vendor evaluation (use a scoping/fit conversation instead).
- For internal transfers or promotions (use the growth-roadmap-generator or a calibration conversation).
- For roles outside the Technology craft without adapting the competency anchor.

---

# Company Context
Look for the company information in `shared/company.md`.

---

# Workflow

Follow these steps in order every time this skill is invoked.

## Step 1 — Extract Role and Level
Identify the role and level from the user's prompt. Normalize to a standard label:
- Examples: `Senior Software Engineer`, `QA Analyst`
- If the level is ambiguous (e.g., user says "developer"), ask for clarification before continuing.

## Step 2 — Load the Competency Table
Look for a matching file in `shared/competencies/`.

- **If found**: Load the competency data. This defines the expected behaviors and skills at that
  level and anchors every section of the interview guide.
- **If not found**: Notify the user:
  > "I don't have a competency table for that role yet. Could you briefly describe what's
  > expected at this level, or paste the relevant competencies? Alternatively, say **'proceed'**
  > and I'll use general engineering expectations for that seniority."
  Wait for their response before continuing.

## Step 3 — Analyze the Prompt
Review everything the user provided. Extract and categorize:

**Role signals**
- Confirmed level and track (IC vs. lead vs. director).
- Any seniority nuances mentioned (e.g., "leaning toward the senior end of M3").

**Project or context signals**
- Specific client industry or domain (e.g., financial services, healthcare, e-commerce).
- Required technologies, frameworks, languages, platforms, or certifications.
- Team composition context (e.g., "this person will be the only FE on the project").
- Timeline pressure or delivery complexity.

**People and culture signals**
- Any team dynamics mentioned (e.g., "we need someone who can mentor a junior").
- Client-facing expectations.
- Any red flags or must-avoids mentioned.

**Gaps**
- Note which competency areas the prompt does not address. These will inform clarifying questions.

## Step 4 — Ask Clarifying Questions
Ask **2–3 targeted questions** to fill the most important gaps from Step 3.
Prioritize questions that would meaningfully change the questions generated.

**Always include this option at the end:**
> "Or, if you prefer, just say **'generate'** and I'll build the guide with what I have."

Good questions to consider (adapt to the situation):
- Who else will be in the interview loop, and what will they cover? (Avoids duplication.)
- Is this a net-new role or a backfill? (Backfills may signal a specific gap to probe.)
- Will this person be client-facing, and if so, how much? (Shapes consulting/influence questions.)
- Are there any non-negotiables — skills or behaviors that would immediately disqualify a candidate?
- What does the onboarding timeline look like? (A person joining a live project in two weeks needs a different profile than someone ramping over three months.)

Wait for the user's answers before proceeding. If the user says "generate" at any point,
skip directly to Step 5.

## Step 5 — Generate the Interview Guide
Using all collected information, produce the interview guide following the
Framework and Output Format sections below.

---

# Interview Question Framework

Questions must collect signal across four dimensions. Every generated guide should
balance coverage across all four, weighted by what matters most for the specific role and level.

## Dimension 1 — Technical Craft
Questions that assess depth and quality of technical knowledge. Anchored to the
"Technical Skills" section of the competency table. Include any project-specific technologies
from the prompt.

Signal to collect:
- Depth of expertise in core technical areas for this role.
- Approach to code quality, testing, and performance.
- Ability to make and articulate architecture decisions.
- Awareness of trade-offs, not just solutions.

## Dimension 2 — Delivery & Process
Questions that assess how the candidate manages work, ambiguity, and complexity.
Anchored to the "Delivery" competency. Especially important in an agency context.

Signal to collect:
- How they scope, estimate, and manage risk.
- How they handle competing priorities or unclear requirements.
- Their relationship with process (Agile, CI/CD, documentation).
- How they communicate progress and problems to the team and stakeholders.

## Dimension 3 — Collaboration & Communication
Questions that assess how the candidate works with others — teammates, cross-functional
partners, and clients. Anchored to "Builds Together" and "Influence" competencies.

Signal to collect:
- How they navigate disagreement or misalignment.
- Whether they elevate others or work in isolation.
- How they communicate technical concepts to non-technical audiences.
- Their approach to feedback — giving and receiving.

## Dimension 4 — Growth Mindset & Ownership
Questions that assess character, accountability, and curiosity. Anchored to
"Cultivates Curiosity" and "Gives a Shit" competencies.

Signal to collect:
- How they respond to failure or missed expectations.
- How they stay current in a fast-moving field.
- Whether they take initiative beyond what's asked.
- Evidence of ownership over outcomes, not just effort.

---

# Output Format

The generated guide must follow this exact structure:

---

## Interview Guide: [Role Title] — [Level]
**Generated for**: [Project or context name, if provided]
**Interview type**: [Technical / Behavioral / Full loop / Panel]
**Suggested duration**: [e.g., 60 minutes]
**Interviewer focus**: [What this guide is scoped to cover — useful if part of a panel loop]

---

### Candidate & Role Snapshot
A 3–5 sentence summary of what this role requires, what success looks like in the first
90 days, and what the non-negotiables are. Written so any interviewer can align quickly
before the call, even without reading the full job description.

---

### Before You Start — Interviewer Notes
3–5 bullet points of practical guidance:
- How to create a welcoming opening that puts the candidate at ease.
- What to listen for across all questions (consistent signals at this level).
- How to handle candidates who over-index on one area vs. another.
- Any known biases to watch for in this type of role evaluation.
- Whether to leave time for candidate questions and what that signals.

---

### Section 1 — Technical Craft
**Suggested time**: [X minutes]
**Competencies covered**: [List from framework]

For each question include:

**Q: [Question text]**
> *What to listen for*: [2–3 specific signals that indicate strong, average, or weak answers]
> *Follow-up*: [One follow-up to probe depth or test for specificity]

Include **3–5 questions** in this section. Mix conceptual and applied. If project-specific
technologies were provided, at least one question must address them directly.

---

### Section 2 — Delivery & Process
**Suggested time**: [X minutes]
**Competencies covered**: [List from framework]

Same question format as Section 1.
Include **2–3 questions**.

---

### Section 3 — Collaboration & Communication
**Suggested time**: [X minutes]
**Competencies covered**: [List from framework]

Same question format as Section 1.
Include **2–3 questions**. At least one must probe client-facing or cross-functional behavior
if the role has any client exposure.

---

### Section 4 — Growth Mindset & Ownership
**Suggested time**: [X minutes]
**Competencies covered**: [List from framework]

Same question format as Section 1.
Include **2 questions**. These are often the most revealing — give them appropriate weight.

---

### Red Flags to Watch For
A bulleted list of 4–6 specific signals that should give the panel pause.
These are grounded in the competency gaps most common at this level and in an agency environment.
Not disqualifiers by default — but signals to discuss in debrief.

Examples of what this section should look like:
- Candidate takes personal credit without mentioning team contribution.
- Cannot articulate *why* they made a technical decision, only *what* they decided.
- Has never worked in an environment with multiple concurrent clients or projects.
- Struggles to describe a failure or deflects blame entirely.

---

### Scoring Rubric
A simple 1–4 scale applied to each dimension:

| Score | Label | What it means |
|-------|-------|----------------|
| 4 | Exceptional | Exceeds expectations for this level. Evidence is specific, unprompted, and shows impact. |
| 3 | Strong | Meets expectations. Clear evidence with some prompting. Consistent across questions. |
| 2 | Mixed | Partial evidence. Meets some expectations but gaps are notable. |
| 1 | Insufficient | Little or no evidence of this competency at the required level. |

Include a **Hiring Recommendation** section at the bottom of the rubric:
- **Strong Yes**: 3–4 across all dimensions, no dimension below 2.
- **Yes with Conditions**: Mostly 3s, one dimension at 2 with a clear onboarding plan.
- **No**: Any dimension at 1, or consistent 2s across the board.

---

### Candidate Questions Decoder
List 3–5 questions the candidate is likely to ask, and what their question signals about
their priorities and mindset. This helps the interviewer respond authentically and
also use the question as additional signal.

Example format:
- *"How does the team handle technical debt?"* → They care about craft and sustainability.
  Look for follow-up questions that show they're thinking about long-term impact, not just
  delivery speed.

---

# Example Prompt

> "Role: Senior Solutions Engineer — UI/Frontend.
> Project context: We're hiring for a mid-size e-commerce client on a 6-month engagement.
> The client is on a tight timeline and the team is small — two FE engineers total.
> This person will work directly with the client's product team and needs to be comfortable
> in client-facing conversations.
> Tech stack: React, TypeScript, Next.js. The client also uses Contentful as their CMS,
> so any experience there is a plus.
> We've had issues in the past with engineers who are technically strong but go quiet
> when things get hard. We want someone who surfaces problems early."
