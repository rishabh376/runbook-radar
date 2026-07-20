# Troubleshooting - runbook-radar

**CrashLoopBackOff**
`kubectl logs deploy/runbook-radar -n runbook-radar --previous`
Usually missing env var or bad config.

**ImagePullBackOff**
GHCR auth secret expired. `kubectl create secret docker-registry ...`

**500s spiking**
Check `/metrics`, then Prometheus alerts. Usually downstream timeout.

**Latency p95 high**
`kubectl get hpa -n runbook-radar` - is it scaling? Check metrics-server.

**OOMKilled**
Bump memory limit in `helm/runbook-radar/values.yaml`. Then find the leak.

**Flux won't sync**
`flux get kustomizations` - usually git repo URL rotated.
