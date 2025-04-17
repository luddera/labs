# Kubernetes Deployments and Pods Examples

This repository contains examples of Kubernetes resource definitions using Infrastructure as Code (IaC) principles. The deployments folder demonstrates various deployment strategies and pod configurations using YAML manifests.

## Structure

The repository contains several Kubernetes manifest files:

### Pod Definitions
- [nginx.yaml](deployments/nginx.yaml): Simple nginx pod configuration with custom labels
- [nginx-docs.yaml](deployments/nginx-docs.yaml): Nginx pod with specific version (1.14.2) and exposed port 80

### Deployment Definitions
- [deploy.yaml](deployments/deploy.yaml): Apache HTTPD deployment with RollingUpdate strategy
  - 10 replicas
  - Rolling update configuration with maxUnavailable: 1 and maxSurge: 1
  - Using httpd:alpine3.19 image

- [deploy-recreate.yaml](deployments/deploy-recreate.yaml): Apache HTTPD deployment with Recreate strategy
  - 10 replicas
  - Using httpd:alpine3.18 image
  - Demonstrates the Recreate deployment strategy

## Key Features Demonstrated

- Different deployment strategies (RollingUpdate vs Recreate)
- Pod configurations with various metadata and labels
- Container image versioning
- Port exposing configuration
- Replica management
- Label selectors for deployments

## Usage

To apply any of these configurations to your Kubernetes cluster:

```bash
kubectl apply -f deployments/<filename>.yaml
```

For example, to create the nginx pod:
```bash
kubectl apply -f deployments/nginx.yaml
```