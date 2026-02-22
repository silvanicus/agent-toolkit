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

- **`shared/company.md`** — A template for describing your organization. Fill it in with your company's identity, size, geography, client model, culture, and tech stack. Skills use this as always-on context to make their output more relevant and specific to your situation.
- **`shared/competencies/<role-slug>.md`** — One file per role (e.g., `senior-ui-engineer.md`), defining the competency framework for that level. Skills reference these to tailor output to the specific role being evaluated or developed. No files exist here yet — add your own as needed.

To customize for your organization:
1. Fill in `shared/company.md` with your real company details, replacing the placeholder text.
2. Add files to `shared/competencies/` for each role you work with, using lowercase-hyphenated filenames (e.g., `senior-ui-engineer.md`).
3. Skills will automatically pick up the new context via the relative paths they reference.

---

## License

MIT
