argocd app create cilium \
--repo git@github.com:devopsjourney1/homelab-services.git \
--path cilium \
--dest-server https://kubernetes.default.svc \
--dest-namespace cilium \
--project default \
--sync-policy automated