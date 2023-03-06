
# Installation

This is the command I used to install ArgoCD on my cluster. It required the insecure flag to work with the ingress proxy.

```
helm install my-argo-cd argo/argo-cd --version 5.3.4 --set server.insecure=true --namespace argocd
```

# Login and add Repo

```
argocd login argocd.devopsbrad.com
argocd repo add git@github.com:devopsjourney1/homelab-services.git --ssh-private-key-path ~/.ssh/id_ed25519
```