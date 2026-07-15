# Architecture decisions

The platform runs a stateless FastAPI service as a non-root Docker container on Amazon EKS. Terraform provisions a two-AZ VPC, private worker subnets, EKS, ECR, IAM roles, CloudWatch log storage, and an alarm. GitHub Actions is the primary cloud-native delivery path; Jenkins demonstrates an enterprise Groovy pipeline.

Reliability controls include replicas, health probes, resource limits, HPA, PodDisruptionBudget, rollout checks, and smoke tests. Prometheus collects application metrics, Grafana displays request rate, latency, and errors, and CloudWatch covers AWS/EKS telemetry.

This is intentionally a portfolio baseline. A true production platform should add three Availability Zones, one NAT gateway per AZ, private EKS endpoint access, ACM/TLS, AWS Load Balancer Controller, ExternalDNS, Secrets Manager, External Secrets, remote Terraform state, policy enforcement, backups, and controlled environment promotion.
