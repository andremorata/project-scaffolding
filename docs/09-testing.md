# Testing Template

> Use this document to define the quality strategy for the project across code, contracts, and delivery stages.

## 1. Testing Goals

Clarify what confidence the team expects from automated and manual validation.

This scaffold assumes testing is a core delivery activity from the beginning of the project, not a stabilization phase after implementation.

## 2. Test Pyramid

| Layer | Purpose | Tooling | Status |
| --- | --- | --- | --- |
| Unit | Fast logic validation | TBD | Open |
| Integration | Component collaboration | TBD | Open |
| Contract | Interface stability | Optional | Open |
| End-to-end | User flow validation | TBD | Open |
| Performance | Capacity or latency confidence | Optional | Open |

## 3. Minimum Required Baseline

Every project created from this scaffold should start with these minimum expectations:

- Unit tests for core business rules, utilities, validators, and isolated components or services
- Integration tests for database behavior, infrastructure boundaries, and backend request handling
- End-to-end tests for the main happy paths and the most business-critical user journeys
- Regression tests for confirmed bugs

Prefer the following workflow:

1. Write a failing test first when the behavior is clear.
2. If discovery is still in progress, implement and tests in tight parallel.
3. Do not merge completed behavior without the tests that give confidence at the appropriate level.

## 4. Ownership

Document who owns:

- unit tests,
- integration environments,
- flaky test triage,
- test data maintenance,
- release signoff.

## 5. Standards

Define:

- required tests per feature type,
- naming conventions,
- fixture strategy,
- mocking guidance,
- coverage expectations,
- and when manual QA is still required.

Recommended default rules:

- Prefer unit tests for fast feedback on pure logic.
- Prefer integration tests for behavior that depends on frameworks, persistence, or wiring.
- Use end-to-end tests sparingly but intentionally for the flows that matter most.
- Avoid pushing all confidence into E2E when cheaper unit or integration tests can cover the same risk.
- When fixing bugs, reproduce the bug with a test before or alongside the fix whenever practical.

## 6. Verification by Delivery Stage

| Stage | Required Validation |
| --- | --- |
| Local development | Relevant unit tests plus any touched integration or UI tests |
| Pull request | Lint, unit tests, and targeted integration tests |
| Merge to main | Full unit and integration suite, plus build validation |
| Pre-release | End-to-end smoke coverage for critical paths |
| Post-deploy | Smoke checks and health verification |

## 7. Test Data and Environments

Capture:

- seed data approach,
- environment isolation,
- external dependency stubbing,
- ephemeral environments if used.

## 8. Frontend and Backend Mapping

Use this as the default minimum split when a project contains both frontend and backend work:

| Area | Minimum Test Expectation |
| --- | --- |
| Backend business logic | Unit |
| Backend persistence and API behavior | Integration |
| Frontend components and hooks | Unit |
| Frontend feature flows | Integration-style UI tests |
| Critical user journeys | End-to-end |

## 9. Open Questions

- Which checks must be standardized across all projects using this scaffold?
- What level of E2E coverage is necessary for the product type?
