# Backend Template

> Use this document to define backend structure, service boundaries, implementation patterns, and operational expectations.

## 1. Backend Mission

Describe what the backend is responsible for in the project:

- business logic,
- orchestration,
- persistence access,
- integrations,
- background jobs,
- and security enforcement.

## 2. Platform Decisions

| Area | Selected Option | Status | Notes |
| --- | --- | --- | --- |
| Runtime / language | TBD | Open | |
| Framework | TBD | Open | |
| API style | TBD | Open | |
| Background jobs | TBD | Open | |
| ORM / data access | TBD | Open | |
| Validation approach | TBD | Open | |
| Testing stack | TBD | Open | |

## 3. Suggested Structure

```text
backend/
├── src/
│   ├── domain/
│   ├── application/
│   ├── infrastructure/
│   └── api/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── contract/
└── scripts/
```

## 4. Minimum Backend Enforcements

Use these as the default starting rules unless the project records a justified exception.

### Architecture

- Prefer Clean Architecture or an equivalent layered modular structure.
- Keep business rules in `domain/` or core modules with no dependency on frameworks, HTTP, databases, or external SDKs.
- Keep use-case orchestration in `application/`.
- Keep persistence, integrations, messaging, and infrastructure concerns in `infrastructure/`.
- Keep transport concerns such as HTTP endpoints, controllers, RPC handlers, or serializers in `api/`.
- Depend inward only. Outer layers may reference inner layers; inner layers must not reference outer layers.

### Development Guidance

- Prefer test-first or test-in-parallel development for new backend behavior.
- Add unit tests for domain logic, value objects, policies, validators, and pure application services.
- Add integration tests for repositories, data access, migrations, message handlers, and full request pipelines where relevant.
- Add regression tests for bug fixes before or alongside the fix whenever practical.
- Keep business logic out of controllers, endpoint classes, and ORM models when possible.

## 5. Design Rules

Document project choices for:

- modular boundaries,
- dependency direction,
- DTO and mapping strategy,
- validation layers,
- error handling,
- async processing,
- transactional behavior,
- idempotency and concurrency,
- configuration management.

### Suggested Dependency Rule

```text
api -> application -> domain
infrastructure -> application and domain
domain -> no outer-layer dependencies
```

## 6. Coding Conventions

Capture standards such as:

- naming conventions,
- folder organization,
- endpoint or handler pattern,
- service and repository expectations,
- background worker conventions,
- eventing strategy if applicable.

## 7. Testing Expectations

Document the concrete backend testing stack once the project chooses tools, but keep this minimum baseline:

- `tests/unit/`: domain and application logic
- `tests/integration/`: database, infrastructure, and API pipeline tests
- `tests/contract/`: external or internal contract verification where useful

Every backend feature should be evaluated against this matrix:

| Change Type | Minimum Expected Test Coverage |
| --- | --- |
| Pure business rule | Unit |
| Persistence or migration change | Integration |
| Endpoint or API contract change | Integration, optionally contract |
| Critical workflow spanning layers | Unit plus integration |

## 8. Security and Reliability

Define:

- authorization enforcement points,
- audit expectations,
- retry policies,
- timeout rules,
- resilience boundaries around external calls.

## 9. Open Questions

- Will the backend start as a single service or a set of bounded modules?
- Which conventions should stay constant across future projects using this scaffold?
