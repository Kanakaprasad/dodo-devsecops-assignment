# Task 1 – Kubernetes Workload Hardening

## Objective

The goal of this task was to deploy the provided application on Kubernetes and improve its security by following production-ready Kubernetes security practices.

## What I Implemented

- Created Kubernetes Deployments and Services for the application.
- Configured ConfigMaps for application configuration.
- Moved sensitive information from plain Kubernetes Secrets to Sealed Secrets.
- Configured containers to run as a non-root user.
- Enabled a read-only root filesystem.
- Dropped unnecessary Linux capabilities.
- Applied the RuntimeDefault seccomp profile.
- Added CPU and memory requests and limits.
- Configured liveness and readiness probes.
- Created a dedicated ServiceAccount instead of using the default account.
- Applied RBAC with least privilege permissions.
- Configured Kyverno policies to prevent insecure workloads such as root containers and latest image tags.

## Design Decisions

I focused on reducing the attack surface of the application without changing its functionality. Security controls were applied at multiple levels, including container runtime security, access control, secret management, and admission policies. This approach helps prevent insecure configurations from being deployed into the cluster.

## Result

The application was successfully deployed with improved security controls, and Kyverno admission policies enforced the required security standards before workloads could be created.
