# Test Argo App

This repository contains a simple test application for Argo CD, a declarative, GitOps continuous delivery tool for Kubernetes.

## Project Structure

The repository consists of the following key files:

- `deployment.yaml`: Defines the Kubernetes deployment for the application
- `service.yaml`: Specifies the Kubernetes service for the application
- `kustomization.yaml`: Configures Kustomize for managing Kubernetes manifests

## Deployment

The `deployment.yaml` file defines a Kubernetes Deployment with the following specifications:

- **Name**: hello-world
- **Replicas**: 1
- **Container**:
  - **Image**: paulsonoflarsnl/hello-world:latest
  - **Port**: 8080

## Service

The `service.yaml` file defines a Kubernetes Service with the following specifications:

- **Name**: hello-world
- **Type**: ClusterIP
- **Port**: 80
- **Target Port**: 8080

## Kustomization

The `kustomization.yaml` file lists the resources to be included in the Kustomize build:

- deployment.yaml
- service.yaml

## Usage

To use this application with Argo CD:

1. Set up Argo CD in your Kubernetes cluster
2. Create an Argo CD Application pointing to this repository
3. Sync the application to deploy it to your cluster

## Contributing

Contributions to improve this test application are welcome. Please submit issues and pull requests on the GitHub repository.

## License

This project is open-source. Please refer to the repository for specific license information.
