# 🚀 GitOps with ArgoCD: Hands-on Guide

Welcome to my GitOps playground! This repository is an experiment where I'm learning and testing out GitOps principles using **ArgoCD** to automate Kubernetes deployments. The key idea behind GitOps is to manage infrastructure and application configuration using **Git** as the source of truth.

This repo demonstrates how developers push code, while ArgoCD pulls and syncs changes to Kubernetes.

## Key Concepts

### 🛠️ Developer Pushes Code

As a developer, you make changes to the application or infrastructure configuration (YAML, Helm charts, etc.) in the Git repository. Once the changes are committed and pushed, the repository becomes the source of truth.

- **Push-to-Git Workflow**: Make changes, commit, and push. Git becomes the single source of truth.
- **Version Control**: Every change is traceable, providing a clear audit trail of all modifications.

### 🔄 ArgoCD Pulls Changes

ArgoCD is a GitOps controller that continuously monitors the Git repository. When it detects any changes, ArgoCD automatically pulls those updates.

- **Declarative Syncing**: ArgoCD pulls the updated manifest files from Git and compares them with the live state in the cluster.
- **Automated Rollbacks**: If something goes wrong, ArgoCD can revert the cluster to the last known good state from Git.

### 🚢 Sync to Kubernetes Cluster

Once ArgoCD pulls the new changes, it applies them to your Kubernetes cluster. This means that your app will always be in sync with the desired state defined in the Git repo.

- **Continuous Deployment**: ArgoCD ensures that your cluster's state always matches what's in Git.
- **Reconciliation**: If the actual state of the cluster drifts from the desired state, ArgoCD will bring it back in line.

## GitOps Flow in Action

1. **Push**: Developer updates a deployment YAML or Helm chart and pushes to Git.
2. **Pull**: ArgoCD notices the new commit, pulls the changes, and updates its internal state.
3. **Sync**: ArgoCD applies the changes to the Kubernetes cluster automatically.
4. **Done**: Your cluster is updated—no manual kubectl or CI pipelines needed!

## Setup

- **ArgoCD**: Set up ArgoCD in your Kubernetes cluster. (Check the official [ArgoCD documentation](https://argo-cd.readthedocs.io/en/stable/) for setup instructions).
- **Git Repository**: This repo contains Kubernetes manifests/Helm charts that will be automatically deployed by ArgoCD.
- **Kubernetes Cluster**: Have a running Kubernetes cluster that ArgoCD can manage.
