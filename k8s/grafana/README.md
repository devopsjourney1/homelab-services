# Grafana

This is a Grafana deployment for Kubernetes. It is deployed via ArgoCD.

### Configuration

Fill out `values.yaml` with the following values.
Refer to https://grafana.github.io/helm-charts for configuration options.

### Acess

Grafana is internal to the cluster with no ingress, I access it using a Zero Trust Access tool called Twingate which gives me access to the applications within my Kubernetes Cluster.

Below are the internal only URLs.

#### Prod:
https://grafana.devopsbrad.com/

#### Dev
https://grafana.dev.devopsbrad.com/