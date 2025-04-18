# Mealie Kubernetes Deployment

This repository contains Kubernetes manifests for deploying [Mealie](https://github.com/mealie-recipes/mealie), a self-hosted recipe manager and meal planner.

## About Mealie

Mealie is a modern, self-hosted recipe management system that allows you to:
- Store and organize your recipes
- Plan your meals
- Create shopping lists
- Share recipes with family and friends

## Repository Structure

- [deployment.yaml](mealie/deployment.yaml): Defines the Mealie application deployment
  - Uses official image `ghcr.io/mealie-recipes/mealie:v2.8.0`
  - Exposes port 9000
  - Single replica deployment
- [namespace.yaml](mealie/namespace.yaml): Creates a dedicated 'mealie' namespace

## Deployment

1. First, create the namespace:
```bash
kubectl apply -f mealie/namespace.yaml
```

2. Deploy the application:
```bash
kubectl apply -f mealie/deployment.yaml
```

## Configuration

- The deployment runs Mealie version 2.8.0
- Application runs on port 9000
- Deployed in a dedicated 'mealie' namespace for better resource isolation

## Note

This is a basic deployment setup. For production use, you might want to consider adding:
- Persistent storage for data
- Environment variables for configuration
- Ingress rules for external access
- Resource limits
- Database configuration