# CI/CD Template

> Use this document to define the continuous integration and delivery pipeline for the project.

## 1. Goals

The pipeline should answer:

- what gets validated,
- when artifacts are built,
- how deployments are promoted,
- and which gates protect quality.

## 2. Pipeline Stages

| Stage | Purpose | Typical Checks |
| --- | --- | --- |
| Lint | Fast feedback | formatting, static analysis |
| Test | Behavioral validation | unit, integration, contract |
| Build | Artifact creation | binaries, containers, bundles |
| Security | Risk checks | dependency and secret scanning |
| Deploy | Environment rollout | staging or production promotion |
| Verify | Post-deploy checks | smoke tests, health checks |

## 3. Trigger Rules

Document expected triggers:

- pull request,
- merge to main,
- release tag,
- manual promotion,
- scheduled validation.

## 4. Artifact Strategy

Define:

- artifact types,
- naming conventions,
- retention,
- provenance,
- rollback readiness.

## 5. Deployment Model

Choose and document:

- trunk-based continuous deployment,
- staged promotion,
- blue/green,
- canary,
- feature-flag-assisted rollout.

## 6. Required Gates

| Gate | Applies To | Required |
| --- | --- | --- |
| Lint | Pull requests | TBD |
| Unit tests | Pull requests | TBD |
| Integration tests | Main / release | TBD |
| Security scan | Main / release | TBD |
| Smoke tests | Post-deploy | TBD |

## 7. Failure Handling

Document:

- ownership for broken pipelines,
- rollback rules,
- flaky test process,
- emergency bypass policy.

## 8. Open Questions

- How automated should production deployment be?
- Which validations are mandatory for all future projects using this scaffold?
