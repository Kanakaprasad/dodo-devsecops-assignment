# Task 3 - Zero Trust Networking with Istio

## Objective

This task secures communication between Kubernetes workloads using Istio service mesh and Kubernetes network policies.

## Implemented Features

- Istio service mesh
- STRICT Mutual TLS (mTLS)
- AuthorizationPolicy
- Kubernetes NetworkPolicy
- Secure service-to-service communication

## Security Controls

### Istio mTLS

- STRICT mode enabled
- Encrypted communication between workloads

### Authorization Policy

- Only authorized services are allowed.
- Unauthorized requests are denied.

### Network Policy

- Restricts unnecessary pod communication.
- Implements least-privilege networking.

## Validation

- Verified secure communication.
- Verified blocked unauthorized traffic.

## Result

Zero Trust networking was successfully implemented using Istio and Kubernetes security policies.
