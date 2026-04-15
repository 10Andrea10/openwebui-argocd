# openwebui-argocd

GitOps bootstrap for Open WebUI on k3s with Argo CD.

Bootstrap once from the server:

```bash
kubectl apply -f bootstrap.yaml -n argocd
```

After that, update the manifests in Git and push:

```bash
git add .
git commit -m "Update Open WebUI configuration"
git push
```

Argo CD will reconcile the repo automatically.
