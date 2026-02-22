# Agent Toolkit

A personal collection of Claude skills, agent templates, scripts, and shared resources I use in my daily work. Made public in case any of it is useful to others.

The toolkit is organized around practical scenarios — things like hiring, performance feedback, and writing — with more being added over time.

---

## What's Inside

```
agent-toolkit/
├── agents/          # Agent templates for specific workflows (coming soon)
├── scripts/         # Utility and automation scripts (coming soon)
├── shared/          # Shared context and resources used across skills
└── skills/          # Claude skills for daily tasks
```

---

## Skills

A collection of skills for AI coding agents. Skills are packaged instructions and scripts that extend agent capabilities.

Skills follow the [Agent Skills](https://agentskills.io/) format.

---

## Shared Resources

The `shared/` folder contains context that multiple skills draw from.

The files here are **samples** — they reflect a specific organizational context used as a reference implementation. When adapting this toolkit for your own company or team, replace them with your own:

- **`shared/company.md`** — Describes your organization: team structure, what the environment rewards, and what "good" looks like. Skills use this to frame questions and evaluation criteria appropriately.
- **`shared/competencies/<role-slug>.md`** — One file per role (e.g., `senior-ui-engineer.md`), defining the competency framework for that level. Skills reference these to tailor output to the specific role being evaluated or developed.

To customize for your organization:
1. Edit `shared/company.md` to reflect your team structure, values, and working style.
2. Add or replace files in `shared/competencies/` for each role you work with, using lowercase-hyphenated filenames.
3. Skills will automatically pick up the new context via the relative paths they reference.

---

## License

MIT
