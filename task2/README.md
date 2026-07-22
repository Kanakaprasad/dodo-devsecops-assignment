# Task 2 - CI/CD Pipeline and GitOps

## Objective

This task implements a secure CI/CD pipeline and GitOps workflow for the Ledger API application.

## Components

- GitHub Actions for Continuous Integration
- Docker image build and publishing
- Trivy container image vulnerability scanning
- Gitleaks secret scanning
- ArgoCD for GitOps deployment
- Automatic synchronization and self-healing

## Workflow

1. Code is pushed to GitHub.
2. GitHub Actions executes the CI pipeline.
3. Security scans are performed.
4. Docker image is built and pushed.
5. ArgoCD detects repository changes.
6. Kubernetes cluster is updated automatically.

## Security Features

- Automated vulnerability scanning
- Secret detection
- GitOps-based deployment
- Automatic reconciliation

## Result

A secure CI/CD pipeline was implemented with automated deployment and continuous security validation.
