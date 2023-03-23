# Install K3s

https://docs.k3s.io/quick-start

- Create a Master
```
curl -sfL https://get.k3s.io | sh -
```

- Creating a Worker nodes
```
CONTROLSERVER_IP=x.x.x.x
curl -sfL https://get.k3s.io | K3S_URL=https://${CONTROLSERVER_IP}:6443 K3S_TOKEN=mynodetoken sh -
```

# Installation

This is the command I used to install ArgoCD on my cluster. It required the insecure flag to work with the ingress proxy.

- Install argocd with helm
```
helm install my-argo-cd argo/argo-cd \
--version 5.27.1 \
--namespace argocd \
--create-namespace \
--values values.yml
```

- Create the ingress proxy
```
kubectl apply -f argo-ingress.yml
```

# Login and add Repo

```
argocd login argocd.devopsbrad.com
argocd repo add git@github.com:devopsjourney1/homelab-services.git --ssh-private-key-path ~/.ssh/id_ed25519
```


# Uninstall K3s
```
/usr/local/bin/k3s-uninstall.sh
```