# FAQ - runbook-radar

**Q: What problem does this actually solve?**
A: Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

Pain point: Failover plans look good in docs but are rarely rehearsed end to end.

**Q: Free to run?**
A: Yep. Render - $0/mo. See `terraform/INFRA_REQUIREMENTS.md`

**Q: Production ready?**
A: Yes - SLOs, security hardening, DR runbook, Helm, Terraform, monitoring.

**Q: Stack?**
A: Go, Prometheus, Grafana, Chaos Mesh, Argo Rollouts, OTel

**Q: What infra do I need?**
A: `terraform/INFRA_REQUIREMENTS.md` has the full breakdown - CPU/RAM/storage/network/cost.
