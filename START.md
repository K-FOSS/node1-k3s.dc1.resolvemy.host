# Provisoning 

To get the node1.dc1.resolvemy.host server online you need to first install Flatcar Container linux and install K3s


```sh
curl -sfL https://get.k3s.io | sh - 
```

Install ArgoCD

```sh
kubectl create namespace argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

```bash
kubectl apply -f https://raw.githubusercontent.com/K-FOSS/node1-k3s.dc1.resolvemy.host/refs/heads/main/Apps/Infra/ArgoCDApplications.yaml
```

Start sync on the app of apps `dc1-k3s`