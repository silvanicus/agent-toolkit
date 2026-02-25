# Agent Toolkit

Agent toolkit repo with multiple skills, plugings, templates and scripts for different purposes.
 This should be used using claude Desktop or Claude code.

Skills follow the [Agent Skills](https://agentskills.io/) format and are designed to be invoked as slash-command-style capabilities by AI coding agents.

## Repository Structure

- `skills/<slug>/SKILL.md` — Individual skills with YAML frontmatter and structured Markdown
- `shared/` — Adding here some templates / samples of shared documents that the skills or agents can use. 
- `agents/` Instructions and other files for the agents. 
- `scripts/` — Using claude for judgement and scripts for execution. 

## Skill File Format

Skills follow the [Agent Skills](https://agentskills.io/) format and are designed to be invoked as slash-command-style capabilities by AI coding agents.

## Gotchas

- Skills reference shared files. Make them generic, as depends on the implementation 
- Skills include a "generate" escape hatch — users can say "generate" at any clarifying-question step to skip ahead.
