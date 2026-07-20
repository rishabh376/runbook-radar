# Deployment - runbook-radar

**Use case:** Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

## Infra requirements
→ `terraform/INFRA_REQUIREMENTS.md` - CPU/RAM/storage/network/cost breakdown

## GitOps
Flux watches `main` and reconciles changes automatically.

## Rollback
```
./scripts/rollback.sh
kubectl rollout undo deploy/runbook-radar -n runbook-radar
```
Usually < 30 sec.

## Cost
Render - $0/mo

Reliability and safety go hand-in-hand: SLO guardrails, incident runbooks, and control-plane failure mode analysis.
