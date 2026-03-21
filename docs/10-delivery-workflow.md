# Delivery Workflow Template

> Use this document to define how work moves from idea to production in a way that humans and AI agents can both follow.

## 1. Delivery Principles

- Keep work small and reviewable.
- Prefer explicit acceptance criteria.
- Tie code changes back to documented decisions.
- Preserve a clear trail from plan to implementation to verification.

## 2. Suggested Flow

1. Define scope in `specs/`.
2. Confirm architecture and operational implications in `docs/`.
3. Implement in small increments.
4. Verify with the testing strategy.
5. Update progress and readiness notes.
6. Deploy through the agreed CI/CD path.

## 3. Work Item Structure

Each feature or phase should ideally include:

- problem statement,
- scope and exclusions,
- acceptance criteria,
- dependencies,
- verification steps,
- documentation impact.

## 4. Definition of Ready

- Goal is understood
- Dependencies are identified
- Open architectural risks are visible
- Acceptance criteria exist
- Required environments or data are available

## 5. Definition of Done

- Implementation complete
- Tests updated and passing at the expected level
- Relevant docs updated
- Operational impact reviewed
- Deployment path understood

## 6. Open Questions

- How formal should phase gating be for the target team?
- Which parts of this workflow should be mandatory for all new projects?
