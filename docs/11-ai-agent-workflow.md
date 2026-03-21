# AI Agent Workflow Template

> Use this document to define how AI agents should operate safely and effectively inside the project.

## 1. Role of AI Agents

AI agents should help with:

- implementation,
- refactoring,
- documentation,
- testing,
- repository cleanup,
- and delivery support.

They should not silently invent product requirements or overwrite human decisions.

## 2. Operating Rules

- Read the relevant docs before making major changes.
- Prefer explicit assumptions over hidden ones.
- Keep changes aligned with architecture and delivery rules.
- Update docs when implementation changes expectations.
- Leave notes when uncertainty remains.

## 3. Handoff Expectations

When an agent finishes a task, it should leave:

- a concise summary of what changed,
- verification performed,
- outstanding risks or assumptions,
- file references where useful.

## 4. Safe Change Boundaries

Document expectations for:

- editing generated files,
- touching infra or deployment config,
- changing public contracts,
- running expensive or destructive commands,
- handling secrets and production identifiers.

## 5. Recommended Inputs for Agents

- task goal,
- relevant files,
- constraints,
- desired verification,
- non-goals,
- and any architectural decisions already made.

## 6. Project-Specific Customization

As the repository becomes a real product, extend this file with:

- coding conventions,
- stack-specific rules,
- review expectations,
- release safety constraints,
- domain terminology.

## 7. Open Questions

- Which agent behaviors should be enforced in all derived projects?
- Which instructions belong here versus in provider-specific files like Copilot or Claude guidance?
