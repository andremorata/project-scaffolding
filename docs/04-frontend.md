# Frontend Template

> Use this document to define the frontend architecture, UX delivery patterns, and client-side standards for the project.

## 1. Frontend Mission

Describe:

- who the primary users are,
- what platforms are supported,
- and which UX qualities matter most.

## 2. Platform Decisions

| Area | Selected Option | Status | Notes |
| --- | --- | --- | --- |
| Web framework | TBD | Open | |
| UI component strategy | TBD | Open | |
| Styling approach | TBD | Open | |
| State management | TBD | Open | |
| Forms | TBD | Open | |
| Data fetching | TBD | Open | |
| Testing | TBD | Open | |

## 3. Suggested Structure

```text
frontend/
├── src/
│   ├── app/ or pages/
│   ├── components/
│   ├── features/
│   ├── hooks/
│   ├── lib/
│   ├── styles/
│   └── types/
├── public/
└── package.json
```

## 4. UI Architecture

Document expectations for:

- routing,
- layout composition,
- design system usage,
- state ownership,
- server/client rendering rules,
- accessibility standards,
- internationalization,
- theme support,
- and performance budgets.

## 5. Minimum Frontend Enforcements

Use these as the default baseline for any new frontend started from this scaffold.

### Development Guidance

- Keep presentation concerns separate from domain and data-access concerns.
- Organize code by feature when the project grows, not only by technical type.
- Prefer reusable UI primitives and shared form/data utilities over duplicated one-off implementations.
- Keep API clients, auth handling, formatting helpers, and state orchestration centralized and testable.
- Prefer test-first or test-in-parallel development for components and user flows with meaningful logic.

### Testing Baseline

- Unit tests are required for non-trivial components, hooks, state utilities, formatters, and validation helpers.
- Integration-style frontend tests are required for forms, async states, and feature modules that combine multiple pieces of UI behavior.
- End-to-end tests are required for primary user journeys, auth flows, and critical regressions once those flows exist.
- Bug fixes should add a regression test at the lowest level that proves the issue stays fixed.

## 6. Screen Inventory

Use this table as the product becomes concrete.

| Route | Area | Purpose | Auth Required | Status |
| --- | --- | --- | --- | --- |
| `/` | Landing | Entry point | TBD | Planned |
| `/app` | Main product | Core workflow | TBD | Planned |
| `/settings` | Preferences | User or org configuration | TBD | Planned |

## 7. Data and State Rules

Define:

- server state approach,
- local UI state rules,
- mutation patterns,
- optimistic updates,
- caching and invalidation,
- error and loading UX,
- form validation behavior.

## 8. Component Guidelines

- Prefer reusable primitives over one-off UI implementations.
- Keep domain logic close to feature modules.
- Centralize formatting, auth, and API utilities.
- Document any design system or component-library decisions explicitly.
- Avoid burying core workflow logic inside large page components when it can be extracted and tested.

## 9. Accessibility and Responsiveness

Set minimum expectations for:

- keyboard access,
- contrast,
- semantic HTML,
- screen reader support,
- touch/mobile behavior,
- reduced motion.

## 10. Open Questions

- Is the product web-only or multi-platform?
- Does the project need SSR, SSG, SPA, or a hybrid model?
- How much UI standardization is expected across future projects?
