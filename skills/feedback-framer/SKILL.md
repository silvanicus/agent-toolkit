---
name: feedback-framer
description: Structures written performance or peer feedback for colleagues and direct reports using the SBI model (Situation → Behavior → Impact). Use when writing review comments in tools like Lattice or Workday, or drafting feedback in email or Slack.
---

# Overview
Turns your observations and notes into structured, competency-anchored written feedback — so every review is consistent, fair, and grounded in what's actually expected at that role and level. Rather than generic comments, this skill anchors your feedback in your organization's competency framework or role expectations, then structures it using the SBI model (Situation → Behavior → Impact). The result is feedback that reflects your standards and reads as credible and actionable.

# When to use this Skill
Use this skill when:
- Structuring written feedback for a colleague or a direct report.
- Writing performance review comments (e.g., in Lattice, Workday, 15Five).
- Drafting peer feedback in an email or Slack message.
- Delivering difficult feedback in a way that is fair and actionable.

# When NOT to use this Skill
- For purely positive praise with no critique needed.
- For informal, casual compliments.
- For disciplinary or HR-sensitive conversations (consult HR/talent directly).

# Workflow

Follow these steps in order every time this skill is invoked:

## Step 1 — Identify the role
Extract the role from the user's prompt. Normalize it to a filename-friendly slug
(e.g., "Senior UI Engineering" → `senior-ui-engineer`).

## Step 2 — Load the competency table
Look for a matching file in `shared/competencies/`.

- **If found**: Read the file and keep the competencies in mind for the rest of the session.
  They define what is expected at that level and should anchor your analysis and questions.
- **If not found**: Tell the user no competency table exists for that role yet, then ask:
  > "Could you briefly describe what is expected at this level, or should I proceed with
  > general engineering/role expectations?"
  Wait for their answer before continuing.

## Step 3 — Analyze the provided information
Review what the user wrote in their prompt. Identify:
- Strengths mentioned (explicit or implied).
- Areas for improvement mentioned (explicit or implied).
- Gaps: competencies from Step 2 that the user did not address at all.

## Step 4 — Ask clarifying questions
Ask **2–4 targeted questions** designed to surface concrete examples, context, or impact
that will make the feedback more specific and credible. Prioritize gaps from Step 3.

**Always include this option at the end of your questions:**
> "Or, if you prefer, just say **'generate'** and I'll create the feedback with what I have."

Good questions to consider (adapt to the situation):
- Can you share a specific situation where [behavior] occurred?
- How frequently does this happen — is it a pattern or more occasional?
- Have you discussed this area with [name] before? What was their reaction?
- How has this affected the team, project, or stakeholders?
- Are there conditions where [name] shows the opposite behavior?

Wait for the user's answers before moving to the next step. If the user says "generate"
at any point, skip directly to Step 5.

## Step 5 — Ask for output format
Before generating, ask the user how they'd like to receive the feedback:

> "How would you like this feedback delivered?
> - **Plain text** — ready to copy and paste into Lattice, Workday, email, or Slack
> - **Markdown** — structured with headers, ideal for Notion, GitHub, or similar tools
> - **Word / Google Doc format** — clean prose paragraphs, easy to drop into a document
> - **PDF-ready** — formatted for export via the `/pdf` skill"

Wait for the user's answer. If the user says "generate" at any point, default to plain text.

## Step 6 — Generate the feedback
Using all collected information, produce the written feedback in the chosen format, following the
Feedback Framework and Output Format sections below.

---

# Feedback Framework
This skill structures feedback using the **SBI model** (Situation → Behavior → Impact):
- **Situation**: Describe the specific context or event.
- **Behavior**: Describe the observable behavior (not assumptions or character judgments).
- **Impact**: Describe the effect that behavior had on you, the team, or the outcome.

# Writing Style Guide
- **Stay close to the user's words.** Preserve the language, phrasing, and specific observations from the original notes as much as possible. Do not paraphrase or sanitize unless necessary for clarity or professionalism.
- **Don't invent examples.** Only use situations, behaviors, and impacts that come from what the user provided or answered in the clarifying questions.
- **Elevate, don't replace.** Your job is to structure and sharpen the user's input, not rewrite it. The voice should still sound like the person giving the feedback.
- **Avoid generic filler.** Phrases like "demonstrates a strong commitment to excellence" or "is a valuable team member" add no signal. Cut them unless they are directly supported by the user's notes.
- **Match the register.** If the user writes casually, keep the tone warm and direct. If they write formally, match that. Do not default to corporate-speak.

# Output Format
Generated feedback will include:
- An opening that acknowledges the person's effort or intent.
- 2–4 specific feedback points following the SBI structure.
- A closing with a forward-looking, encouraging statement.

# Example Prompt
> "Name: Jamie.
> "Role: Senior UI engineering.
> "Context: Lattice perfomance review
> "I think she is accountable and based on the feedback I have had from QA, her deliverables are usually fast, in really good quality. Technically she is senior and shows a really good understanding and skills around quality engineering, accesibility and design systems.
> The only aspect I will improve is that she is too quite and she is not involved in a lot of conversations around solutions, blockers, etc.
> Althogh this is not a requirement for his role, usually senior engineers try to participate more in the solutioning of the different tickets and during daily, participate in different conversations around best practices, requirements, etc.
>With her knowledge, she could be more impactful in a project and a team."
