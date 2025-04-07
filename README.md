# OpenShift AI Installation with GitOps

This repository provides a step-by-step guide to installing OpenShift AI using a GitOps approach with ArgoCD on OpenShift.

## Installation

The installation process consists of the following steps:

> 💡 **Note**: if any of the listed operators are already present in the cluster, you can skip that step.

- Install OpenShift GitOps (ArgoCD)  
- Install ODF (or any other compatible storage provider)  
- Install OpenShift AI

### OpenShift GitOps

If ArgoCD is not already installed, the first step is to install it. To do so, go to the OpenShift Marketplace and install the **OpenShift GitOps** operator.

### OpenShift Data Foundation (ODF)

Similarly, if ODF is not installed in the cluster, proceed with its installation through the Marketplace. Alternatively, you may use another compatible storage provider.

### Bootstrap

Once ArgoCD is installed, apply the ArgoCD *bootstrap* application:

```bash
oc apply -f bootstrap
```