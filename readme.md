# Pre-requisites
Kubernetes cluster is installed and running

# ArgoCD
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
cd argocd && kubectl kustomize apply -k .
```

# Login - ArgoCD
`kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo`

`kubectl port-forward -n argocd svc/argocd-server 8080:80`


# Add app to ArgoCD dashboard
Uncomment app(s) in argocd/kustomization.yaml