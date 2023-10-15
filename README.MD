# Referência para criação de um cluster EKS via crossplane


## Instalação do Autoscaler

No futuro esta parte será adaptada para instalação via argo-cd

```bash
helm repo add autoscaler https://kubernetes.github.io/autoscaler

helm search repo cluster-autoscaler

```

```bash
helm install autoscaler \
--namespace kube-system \
--version 9.29.3 \
--values cluster-autoscaller/helm-values.yaml \
autoscaler/cluster-autoscaler

```