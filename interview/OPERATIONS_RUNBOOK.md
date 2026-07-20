# Operations Runbook - runbook-radar

Service Reliability Owners coordinate validate failover readiness for latency-sensitive gateways, so risky releases pause before budget exhaustion.

**On-call? Read this first.**

## Deploy
```
kubectl apply -k k8s/ -n runbook-radar
kubectl rollout status deploy/runbook-radar -n runbook-radar
```

## Rollback (when things go red)
```
./scripts/rollback.sh
# usually < 30sec
```

## Scale up NOW
```
kubectl scale deploy/runbook-radar --replicas=10 -n runbook-radar
```

## Logs
```
kubectl logs -l app=runbook-radar -n runbook-radar -f --tail=200
```

## Crashloop?
```
kubectl describe pod -l app=runbook-radar -n runbook-radar
kubectl logs <pod> --previous -n runbook-radar
```
90% of the time: missing env var in ConfigMap.

## Metrics
`curl localhost:8080/metrics` or Grafana dashboard in `monitoring/`

## DR / Failover
See `docs/DISASTER_RECOVERY.md` - RTO 15m

We actually tested this. 11 min.
