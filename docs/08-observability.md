# Observability Template

> Use this document to define how the project will be monitored, debugged, and operated in production.

## 1. Objectives

Observability should help the team:

- detect failures,
- understand behavior,
- troubleshoot quickly,
- and measure reliability.

## 2. Signals

| Signal | Purpose | Tooling | Status |
| --- | --- | --- | --- |
| Logs | Event and error diagnosis | TBD | Open |
| Metrics | Health and trend monitoring | TBD | Open |
| Traces | Request and dependency flow | TBD | Open |
| Alerts | Operational response | TBD | Open |

## 3. Logging Standards

Define:

- structured logging expectations,
- correlation identifiers,
- sensitive data rules,
- log levels,
- retention policy.

## 4. Metrics and SLOs

Document the core indicators:

- availability,
- latency,
- error rate,
- throughput,
- queue depth,
- business KPIs where relevant.

## 5. Tracing

Describe:

- trace propagation strategy,
- external dependency coverage,
- background job instrumentation,
- frontend-to-backend correlation if applicable.

## 6. Alerting

Capture:

- paging thresholds,
- ownership,
- severity model,
- alert fatigue safeguards,
- runbook links.

## 7. Operational Readiness Checklist

- Health endpoints defined
- Dashboards created
- Error reporting configured
- Alerts routed
- Runbooks linked
- Release verification steps documented

## 8. Open Questions

- Which tools are standard across projects?
- What minimum observability is required before production launch?
