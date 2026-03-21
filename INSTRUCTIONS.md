# AI Project Scaffold - Copilot Instructions

You are working inside a reusable project scaffold intended to bootstrap new software products with AI-agent support.

Your job is to help turn this scaffold into a concrete project without introducing assumptions that belong to a previous product.

**IMPORTANT**: THIS IS THE BASE INSTRUCTIONS FILE FOR IA AGENTS WORKING IN THIS REPOSITORY AND `CLAUDE.md`, `.codex/AGENTS.md`, AND `.github/copilot-instructions.md` FILES ARE SYMLINKS TO THIS FILE. DO NOT EDIT THOSE FILES DIRECTLY. IF YOU WANT TO CHANGE THE INSTRUCTIONS, EDIT THIS FILE AND THE CHANGES WILL BE REFLECTED IN ALL SYMLINKS AUTOMATICALLY.

## Core Principles

- Treat this repository as a neutral foundation, not as an existing product.
- Prefer reusable patterns over domain-specific implementation shortcuts.
- Document decisions clearly when a project-specific choice is made.
- Keep architecture, delivery, and operational concerns aligned across code and docs.
- When a placeholder exists, either preserve it or replace it with an explicit project decision. Do not invent hidden defaults.
- Default to clean boundaries, testable code, and explicit verification.

## Preferred Workflow

1. Read the relevant files in `docs/` and `specs/` before making structural changes.
2. Identify whether the task is scaffold-level or project-specific.
3. Preserve reusable guidance and remove stale assumptions from previous projects.
4. Update documentation whenever code, infrastructure, or workflows materially change.
5. Leave the repository easier for the next human or agent to understand.

## Specs-Driven Execution

The `specs/` folder is the execution backbone of the project. Agents must treat it as the authoritative source for delivery sequencing and scope control.

### Required files in `specs/`

- `project-template.plan.md` or the project-specific plan file:
  the master plan for phases, scope, sequencing, and major delivery expectations
- `phase-template.issue.md` or the active phase issue files:
  the actionable breakdown for a single phase, milestone, or workstream
- `progress.status.md`:
  the source of truth for current status, validation state, evidence, and next actions

### Required agent behavior

Before doing substantial work:

1. Read the project plan in `specs/` to understand the intended roadmap.
2. Identify the active phase or the phase most directly related to the request.
3. Read the corresponding phase issue file before implementing changes.
4. Check `progress.status.md` to understand the current state, risks, and validation status.

While doing the work:

- Stay aligned with the current plan and phase scope unless the user explicitly changes direction.
- Do not silently implement work that belongs to a later phase if it changes scope, architecture, or delivery order in a meaningful way.
- If the requested change requires deviating from the plan, update the relevant `specs/` files as part of the task or clearly document the mismatch.
- Keep implementation, docs, and progress tracking synchronized.

After completing meaningful work:

- Update the relevant phase issue if scope, tasks, acceptance criteria, or notes changed.
- Update `progress.status.md` when phase status, evidence, risks, or next actions changed.
- Reference the plan and phase context in summaries so future agents can continue from the intended roadmap.

### Precedence inside `specs/`

Use this order when interpreting project intent:

1. Active user instruction
2. The project plan in `specs/`
3. The relevant phase issue file
4. `progress.status.md`

If these conflict, do not guess silently. Align the files as part of the task or call out the mismatch clearly.

## What This Scaffold Should Cover

- Backend architecture and service boundaries
- Frontend architecture and UX delivery conventions
- Database and persistence guidance
- Infrastructure and environment strategy
- CI/CD pipeline design
- Observability and operational readiness
- Testing strategy across layers
- Delivery phases, progress tracking, and readiness gates
- AI-agent collaboration rules and handoff expectations

## Guardrails

- Do not hardcode domain language unless the current project has explicitly chosen it.
- Do not assume a specific stack unless documented in the active architecture decisions.
- Do not leave orphaned references to previous systems, modules, entities, or brands.
- Prefer templates, placeholders, checklists, and decision records when requirements are still open.
- Do not ignore the `specs/` plan, phase, or progress files when they exist for the active project.

## Documentation Expectations

When creating or editing docs:

- Use clear section headings and checklists.
- Separate confirmed decisions from open questions.
- Keep examples generic unless the repository already defines a concrete stack.
- Note dependencies between architecture, infrastructure, testing, and delivery decisions.
- Keep `docs/` aligned with the current phase plan and update `specs/` when documentation changes affect scope or sequencing.

## Coding Expectations

When source code exists:

- Follow the architecture and testing rules documented for the active project.
- Keep implementation consistent with CI/CD and observability expectations.
- Add or update tests for behavior changes.
- Avoid introducing tooling that conflicts with documented delivery workflows.
- Use the active project plan and phase issue as the default boundary for what should be implemented now.

Unless the project documents a different choice, assume these defaults:

- Use Clean Architecture or similarly strict modular boundaries for backend work.
- Keep domain or core logic independent from UI, transport, and infrastructure concerns.
- Treat unit, integration, and end-to-end testing as part of the minimum delivery baseline.
- Prefer test-driven or test-in-parallel development for non-trivial features and bug fixes.
- Add regression tests for defects at the most appropriate level.

## If the Repository Is Still in Template Mode

In template mode, optimize for:

- clarity,
- reusability,
- low-coupling documentation,
- and smooth project kickoff.

Even in template mode, keep the `specs/` workflow explicit so future projects inherit a plan-first execution model.
