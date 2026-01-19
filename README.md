# app-gitops-bgd

This repository demonstrates GitOps principles by defining Kubernetes applications that can be managed using tools like ArgoCD.

## Repository Structure

### Application Definition (`apps`)
The `apps` directory contains Kubernetes manifests for applications such as `bgd`. These manifests include:
- **Deployments**: Definitions for application workloads.
- **Namespaces**: Resources to isolate applications.
- **Kustomize Configurations**: Aggregates resources for deployment.

### Cluster Configuration (`clusters`)
The `clusters` directory contains provisioning files for different clusters and environments, such as:
- **Development Clusters**: Configuration for development environments.
- **Test Clusters**: Configuration for testing environments.

## GitOps Workflow
This repository is designed to work with ArgoCD using a Git generator. ArgoCD monitors the repository and deploys applications to the appropriate clusters and environments based on the configuration.

## Usage
1. Configure ArgoCD to monitor the `apps` directory.
2. Use the `clusters` directory to define cluster-specific configurations.
3. Commit changes to the repository, and ArgoCD will automatically apply them to the clusters.

