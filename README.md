# Dodo Payments – Security & DevOps Engineer Technical Assessment

## Overview

This repository contains my solution for the Dodo Payments Security & DevOps Engineer technical assessment.

The assignment focuses on securing a cloud-native application by applying Kubernetes security best practices, building a secure CI/CD pipeline, implementing Zero Trust networking with Istio, and performing reconnaissance and penetration testing on the provided application.

All tasks were completed using a local Kubernetes environment and open-source tools.

## Repository Structure

- **task1/** – Kubernetes workload hardening
- **task2/** – Secure CI/CD pipeline and GitOps
- **task3/** – Istio service mesh and Zero Trust implementation
- **task4/** – Reconnaissance, penetration testing, and security assessment report

## Tools & Technologies

- Kubernetes (Kind)
- Docker
- GitHub Actions
- ArgoCD
- Kyverno
- Istio
- Sealed Secrets
- Trivy
- Semgrep
- Gitleaks
- Cosign
- Burp Suite Community
- OWASP ZAP
- Nuclei
- Subfinder
- Amass
- Assetfinder
- WhatWeb
- httpx
- testssl.sh

## Task Summary

### Task 1
Hardened the Kubernetes deployment by applying least-privilege principles, security contexts, RBAC, Sealed Secrets, and Kyverno admission policies.

### Task 2
Built a secure GitHub Actions pipeline with automated security scanning, image signing, and GitOps deployment using ArgoCD.

### Task 3
Configured Istio with STRICT mTLS, identity-based Authorization Policies, and Kubernetes Network Policies to implement Zero Trust networking.

### Task 4
Performed passive reconnaissance on the assigned domain and conducted an authorized penetration test against the provided vulnerable application. Findings and remediation are documented in the Task 4 report.
