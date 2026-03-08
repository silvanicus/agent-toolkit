# Knowledge Base Index

> **Last updated:** YYYY-MM-DD | **Maintainer:** [Team/Person] | **Total docs:** [count]

## How to use this index

**Read this file FIRST for any question about our technology stack.** This index maps every document in the knowledge base. Use it to identify which file(s) to consult, then reference those files for detailed information.

If a topic spans multiple documents, check the Cross-References section for common combinations.

---

## Technologies & Frameworks

| Technology | File | Category | Status | Use Case |
|-----------|------|----------|--------|----------|
| Next.js | `frameworks/nextjs.md` | Framework | Active | Customer-facing web apps |
| React | `frameworks/react.md` | Library | Active | UI component development |
| Vue 3 | `frameworks/vue.md` | Framework | Evaluating | Internal tools (pilot) |
| TypeScript | `languages/typescript.md` | Language | Active | All frontend projects |
| Node.js | `languages/nodejs.md` | Runtime | Active | API services, build tools |

## Design System & UI

| Topic | File | Category | Status |
|-------|------|----------|--------|
| Design Tokens | `design-system/tokens.md` | Foundation | Active |
| Base UI Components | `design-system/base-components.md` | Components | Active |
| Component Patterns | `design-system/patterns.md` | Guidelines | Active |
| Figma Integration | `design-system/figma-workflow.md` | Process | Active |

## Tooling & Infrastructure

| Tool | File | Category | Status |
|------|------|----------|--------|
| Vite | `tooling/vite.md` | Build | Active |
| Vitest | `tooling/vitest.md` | Testing | Active |
| Playwright | `tooling/playwright.md` | E2E Testing | Active |
| Storybook | `tooling/storybook.md` | Documentation | Active |
| ESLint | `tooling/eslint.md` | Linting | Active |
| GitHub Actions | `infrastructure/ci-cd.md` | CI/CD | Active |
| Vercel | `infrastructure/deployment.md` | Hosting | Active |

## Standards & Practices

| Standard | File | Scope | Mandatory |
|----------|------|-------|-----------|
| Coding Standards | `standards/coding-standards.md` | All teams | Yes |
| Accessibility (WCAG 2.1 AA) | `standards/accessibility.md` | All teams | Yes |
| Testing Strategy | `standards/testing-strategy.md` | All teams | Yes |
| Git Workflow | `standards/git-workflow.md` | All teams | Yes |
| Code Review | `standards/code-review.md` | All teams | Yes |
| Performance Budgets | `standards/performance.md` | Customer-facing | Yes |
| Security Practices | `standards/security.md` | All teams | Yes |

## Architecture Decisions (ADRs)

| ID | Decision | File | Date | Status |
|----|----------|------|------|--------|
| ADR-001 | Framework Selection | `decisions/adr-001-framework-selection.md` | 2024-03 | Accepted |
| ADR-002 | State Management | `decisions/adr-002-state-management.md` | 2024-05 | Accepted |
| ADR-003 | Monorepo Strategy | `decisions/adr-003-monorepo.md` | 2024-06 | Accepted |
| ADR-004 | Authentication Approach | `decisions/adr-004-auth.md` | 2024-07 | Accepted |
| ADR-005 | Design Token Architecture | `decisions/adr-005-design-tokens.md` | 2024-08 | Proposed |

## Processes & Workflows

| Process | File | Audience |
|---------|------|----------|
| New Project Setup | `processes/new-project-setup.md` | All developers |
| Onboarding Guide | `processes/onboarding.md` | New team members |
| Release Process | `processes/release.md` | All developers |
| Incident Response | `processes/incident-response.md` | On-call engineers |
| RFC Process | `processes/rfc-process.md` | All teams |

---

## Cross-References

These are common query patterns that span multiple documents:

| If you're asking about... | Consult these files |
|--------------------------|-------------------|
| Starting a new project | `processes/new-project-setup.md` → relevant framework file → `standards/coding-standards.md` |
| Choosing a technology | Relevant ADR → `standards/` guidelines → framework comparison files |
| Deployment & hosting | `infrastructure/deployment.md` + `infrastructure/ci-cd.md` |
| Testing approach | `standards/testing-strategy.md` + tool-specific files (`vitest.md`, `playwright.md`) |
| Component development | `design-system/base-components.md` + `design-system/patterns.md` + `tooling/storybook.md` |
| Performance optimization | `standards/performance.md` + framework-specific gotchas |
| Accessibility compliance | `standards/accessibility.md` + `design-system/base-components.md` |
| Security requirements | `standards/security.md` + `infrastructure/deployment.md` |

---

## Status Legend

| Status | Meaning |
|--------|---------|
| **Active** | In production use, fully supported |
| **Evaluating** | Under evaluation, not for production yet |
| **Proposed** | Decision pending review/approval |
| **Accepted** | Decision approved and in effect |
| **Deprecated** | Being phased out, avoid for new work |
| **Superseded** | Replaced by a newer decision |

---

## Contributing

To add or update documentation:
1. Follow the template in `_templates/technology-template.md`
2. Open a PR with your changes
3. Update this index file with new entries
4. Tag the knowledge base maintainer for review
