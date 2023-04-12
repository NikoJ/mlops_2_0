# Clickhouse operator

## Add the repo

```
helm repo add clickhouse-operator https://docs.altinity.com/clickhouse-operator/
helm repo update
```

## Install the chart

```
helm upgrade -i clickhouse-operator --namespace=kube-system clickhouse-operator/altinity-clickhouse-operator --version 0.20.1
```

## Uninstall the chart


`helm uninstall clickhouse-operator --namespace=[NAMESPACE]`

* [NAMESPACE] is the namespace for the kubernetes. 

Example: `helm uninstall clickhouse-operator --namespace=kube-system`

# Run instanse

`kubectl apply -k .`

>Port Forwarding: `kubectl port-forward service/clickhouse-ch 8123:8123 -n dev`
