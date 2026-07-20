# Setup - runbook-radar

Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

1. **Infra first**: `cd terraform && terraform init && terraform apply`
2. `kubectl apply -k k8s/ -n runbook-radar`
3. `kubectl port-forward svc/runbook-radar 8080:80 -n runbook-radar`
4. `curl localhost:8080/healthz`

Env vars: `PORT=8080`, `LOG_LEVEL=info`

We treat observability as a first-class citizen with alerts tuned to what actually matters in an outage.
