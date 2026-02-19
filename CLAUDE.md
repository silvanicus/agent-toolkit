# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a content-only repository — no code, no build system, no tests, no dependencies. It contains Claude AI skills, shared context resources, and (planned) agent templates and scripts. All files are Markdown.

Skills follow the [Agent Skills](https://agentskills.io/) format and are designed to be invoked as slash-command-style capabilities by AI coding agents.

## Repository Structure

- `skills/<slug>/SKILL.md` — Individual skills with YAML frontmatter and structured Markdown
- `shared/company.md` — Organizational context referenced by skills via relative path
- `shared/competencies/<role-slug>.md` — Role competency frameworks (lowercase-hyphenated slugs, e.g. `senior-ui-engineer`)
- `agents/` and `scripts/` — Reserved for future use (currently empty)

## Skill File Format

Every `SKILL.md` must include:

**YAML frontmatter:**
- `name`: machine-readable slug (e.g., `english-editor`)
- `description`: one-sentence summary of when to invoke the skill

**Markdown sections (in order):**
1. Overview
2. When to use this Skill / When NOT to use this Skill
3. Workflow (numbered steps)
4. Framework (the methodology applied, e.g. SBI feedback model)
5. Output Format (exact structure for generated output)
6. Example Prompt

## Key Conventions

- Skills reference shared files using relative paths (`shared/company.md`, `shared/competencies/<role-slug>.md`). When creating a skill that references a role's competencies, ensure a matching file exists in `shared/competencies/`.
- Skills include a "generate" escape hatch — users can say "generate" at any clarifying-question step to skip ahead.
- Naming uses lowercase-hyphenated slugs throughout (skill directories, competency filenames, frontmatter `name` field).
