# Run Argo Wokflow

1) `kubectl create namespace argo`

2)

```console 
kubectl apply -n argo -f https://github.com/argoproj/argo-workflows/releases/download/v3.4.3/install.yaml
```
3)

```console
kubectl patch deployment \
  argo-server \
  --namespace argo \
  --type='json' \
  -p='[{"op": "replace", "path": "/spec/template/spec/containers/0/args", "value": [
  "server",
  "--auth-mode=server"
]}]'
```

4) `kubectl -n argo port-forward deployment/argo-server 2746:2746`
