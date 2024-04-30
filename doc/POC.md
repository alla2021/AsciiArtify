# Proof of Concept (PoC) for AsciiArtify with ArgoCD

In this Proof of Concept (PoC), we demonstrate the deployment of ArgoCD on a Kubernetes cluster recommended for AsciiArtify.

## Accessing ArgoCD Dashboard

To access the ArgoCD dashboard, follow these steps:

1. Make sure you have `kubectl` configured to access your Kubernetes cluster.

2. Retrieve the ArgoCD server URL:
   ```bash
   kubectl get svc -n argocd argocd-server

3. Obtain the ArgoCD server password:

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
