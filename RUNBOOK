# Operations runbook

## Failed deployment
Run `kubectl -n devops-portfolio rollout status deployment/portfolio-api`, inspect events and pod logs, then use `kubectl -n devops-portfolio rollout undo deployment/portfolio-api` when the release caused the failure.

## High errors or latency
Check Grafana and Prometheus, correlate logs using `x-request-id`, compare the incident start with deployment history, and roll back before doing deeper debugging when customer impact exists.

## Pending pods
Check node capacity, requests and limits, taints, scheduling events, image pull errors, and service-account permissions.

## Cost warning
EKS, EC2 worker nodes, NAT Gateway, load balancers, and CloudWatch incur charges. Destroy the dev environment when it is not being used.
