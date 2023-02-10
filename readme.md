# GitOps
Agnostic Methodology that users GIT repositories as a source of truth for managing infrastructure.

## Basics

Their 3 main pilars:
- Git as single source of truch
- Treat everything as Code
- Operations through Git Workflows

Gitops Principles
- Declarative: a system managed by Gitops should have its state fined declaratively
- Versioned and immutable: The desired state of infrastructure is kept in a way which enforces immutability. Versioning retains a complete version history.
- Pulled automatically: Software agents automatically pull the infrastructure state.
- Continuously reconciled: Software agents study and attempt to keep the system in the desired state.

## Why Gitops
Using GIT which developers are used with operations, helps in unifying both sides of deployments, and make it easier for keeping up with changes and increasing security as unwanted changes are more controlled.

Benefits:
- Standard Workflow: Familiar tools and GIT workflows from app development teams.
- Enhanced security: Changes are easier to trace, making it harder for drifting.
- Visibility and audit: All changes are submitted through issues, branches which allows for better traceability when changing the infrastructure.
- Multi-Cluster consistency: Reliably being able to spin up multiple Kubernetes clusters and environments with one source of truth.

## Kubernetes CI/CD
Continuos integration and deployment are methods to automate app delivery by introducing automation into the stages of development.

Normally, CI takes care of build/security testing and set application boundaries if required. CD takes care of applying infrastructure as code, security or framework boundaries. Gitops focuses on Continuos Deployment and works together with CI to deploy apps.

``` bash
build >> test >> Security Checks >> Release >> Deploy Stage >> Deploy Prod
<--------Continuos Integration -------------->
<--------Continuos Delivery --------------------------------------------->
```

## App deployment with Gitops in K8s

https://developer.hashicorp.com/terraform/tutorials/kubernetes/gke

gcloud services enable pubsub.googleapis.com


- The application deployment model on Kubernetes can be either in-cluster or external
  - external GitOps tool can use Kubernetes just as a target platform for deploying apps.
- In-cluster approaches run a GitOps engine inside Kubernetes to deploy apps and sync manifests in one or more Kubernetes clusters.

For provisioning demo -> go to gke-cluster for initialization
- Compute engine should be initialized in project
- kubernetes api engine

