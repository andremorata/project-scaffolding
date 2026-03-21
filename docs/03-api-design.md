# API Design Template

> Use this document to define service contracts and integration rules for the project.

## 1. API Scope

Capture:

- public versus internal APIs,
- protocol choices,
- versioning strategy,
- auth model,
- and response conventions.

## 2. API Inventory

| API | Audience | Protocol | Status |
| --- | --- | --- | --- |
| Primary application API | Frontend / clients | TBD | Open |
| Admin / internal API | Internal users or ops | Optional | Open |
| Webhooks | External integrations | Optional | Open |

## 3. Core Standards

Define the project choices:

- REST, GraphQL, gRPC, RPC, or hybrid
- Base path conventions
- Resource naming rules
- Pagination style
- Filtering and sorting rules
- Idempotency expectations
- Error envelope format

## 4. Authentication and Authorization

Document:

- auth mechanism,
- token/session model,
- required headers,
- role/permission model,
- rate-limiting expectations,
- machine-to-machine access rules.

## 5. Endpoint Template

Use this format for each area:

| Method | Path | Purpose | Auth | Notes |
| --- | --- | --- | --- | --- |
| `GET` | `/api/example` | List resources | TBD | |
| `POST` | `/api/example` | Create resource | TBD | |
| `GET` | `/api/example/{id}` | Get resource | TBD | |
| `PUT` | `/api/example/{id}` | Update resource | TBD | |
| `DELETE` | `/api/example/{id}` | Delete resource | TBD | |

## 6. Request / Response Examples

```json
{
  "id": "example-id",
  "name": "Example Name",
  "status": "active"
}
```

## 7. Error Handling

Define:

- validation response format,
- domain error translation,
- auth failures,
- rate limits,
- downstream dependency failures,
- trace or correlation identifiers.

## 8. Integration Concerns

Document:

- webhook signing,
- retries,
- idempotency keys,
- eventual consistency behavior,
- external API dependencies,
- backward compatibility rules.

## 9. Change Management

- Where contract changes are proposed:
- How breaking changes are reviewed:
- How API documentation is published:
- How generated clients, if any, stay synchronized:

## 10. Open Questions

- Does the project need a single API surface or multiple bounded interfaces?
- Will third parties integrate directly with the system?
- What compatibility window is required between frontend and backend deployments?
