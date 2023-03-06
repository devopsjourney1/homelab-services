
# Installation

This is the command I used to install ArgoCD on my cluster. It required the insecure flag to work with the ingress proxy.

```
helm install my-argo-cd argo/argo-cd --version 5.3.4 --set server.insecure=true --namespace argocd
```