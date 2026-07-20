# runbook-radar

> Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

**Domain:** sre | **Complexity:** intermediate | **Stack:** Go, Prometheus, Grafana, Chaos Mesh, Argo Rollouts, OTel

| | |
|---|---|
| Use case | Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion. |
| Pain point | Failover plans look good in docs but are rarely rehearsed end to end. |
| Success metric | Validate regional failover monthly with RTO under 90 seconds. |
| Cost | $0/mo on Render |

## Why this exists

Failover plans look good in docs but are rarely rehearsed end to end.. Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

> This production platform is designed for reliability, error budgets, and repeatable recovery drills. For this implementation, the service is designed to remove the operational friction behind Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion..

## What this product does

This project ships a production-oriented service that exposes health, readiness, observability, and domain-specific endpoints for Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.. The implementation is intended to be deployed behind Kubernetes with secure defaults, CI validation, and rollback-ready manifests.

## Quick start

```bash
docker build -t runbook-radar:local .
docker run -p 8080:8080 runbook-radar:local
curl http://localhost:8080/healthz
```

## Architecture

```
GitHub CI -> Container Registry -> Kubernetes -> Go -> Operators / SRE
```

See `docs/ARCHITECTURE.md`

## Infrastructure

Full spec: `terraform/INFRA_REQUIREMENTS.md`

TL;DR: K8s cluster, 2-10 pods HPA, $0 on Render

## Docs

- `docs/ARCHITECTURE.md` - components, tradeoffs
- `docs/DESIGN_DISCUSSION.md` - how we decided to build this
- `docs/DEPLOYMENT.md` - GitOps, rollback
- `docs/SECURITY.md` - threat model
- `docs/TROUBLESHOOTING.md` - 3am runbook
- `terraform/INFRA_REQUIREMENTS.md` - **infra: CPU/RAM/storage/cost**

Interview prep: `interview/`
