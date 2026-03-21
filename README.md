# AI Project Scaffolding

Reusable repository scaffolding for starting new software projects with strong support for AI-assisted delivery.

This base is intentionally product-neutral. It keeps the structure, standards, planning assets, and agent instructions that help a team start fast, while leaving domain rules, data models, and feature scope open for the next project.

## What This Scaffold Includes

- Architecture and engineering decision templates
- Data, API, backend, frontend, and business-rules documentation starters
- Infrastructure, CI/CD, observability, testing, and delivery guidance
- Planning and phase-tracking documents for new project kickoff
- AI agent instructions for consistent implementation behavior
- Editor and repository defaults that work well in multi-stack monorepos

## Current Repository Purpose

Use this repository as a clean starting point when creating a new project from the ground up.

The expected workflow is:

1. Copy or clone this scaffold into a new repository.
2. Rename the project references in the root docs and instructions.
3. Replace placeholder decisions with project-specific choices.
4. Add source folders (`backend/`, `frontend/`, `infra/`, etc.) as the implementation begins.
5. Keep the agent instructions and delivery docs aligned with real architecture decisions.

## Suggested Top-Level Structure

```text
.
├── .github/
│   ├── copilot-instructions.md
│   └── workflows/
├── docs/
│   ├── 01-architecture.md
│   ├── 02-database.md
│   ├── 03-api-design.md
│   ├── 04-frontend.md
│   ├── 05-business-rules.md
│   ├── 06-infrastructure.md
│   ├── 07-cicd.md
│   ├── 08-observability.md
│   ├── 09-testing.md
│   ├── 10-delivery-workflow.md
│   ├── 11-ai-agent-workflow.md
│   └── 12-backend.md
├── specs/
│   ├── project-template.plan.md
│   ├── phase-template.issue.md
│   └── progress.status.md
├── .editorconfig
├── .gitignore
├── CLAUDE.md
└── README.md
```

## How To Adapt It

- Keep sections that are universally useful: standards, delivery stages, documentation templates, and agent operating rules.
- Remove or replace placeholders as soon as real project constraints are known.
- Prefer documenting decisions once in `docs/` and referencing them from issues, plans, and agent instructions.

## Cleanup Status

This version has been cleaned to remove product-specific financial and tenant-management assumptions from the scaffold itself.
