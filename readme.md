# ArgoCD
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

# Add ArgoCD to ArgoCD Dashboard
Copy the content of argocd/apps/argocd.yaml file and add to the dashboard using yaml option
# Add app to ArgoCD dashboard
Uncomment app(s) in argocd/kustomization.yaml