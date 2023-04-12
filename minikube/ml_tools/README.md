# Install

>Run these commands from the directory with yaml

Steps:

1. Postgres:

- `kubectl apply -k .`

>Port Forwarding: `kubectl port-forward service/mlflow-postgres-service 5432:5432 -n dev`

2. Minio:

- `kubectl apply -k .`

>UI: `kubectl port-forward service/mlflow-minio-service 9090:9090 -n dev`

>Port Forwarding: `kubectl port-forward service/mlflow-minio-service 9000:9000 -n dev`

3. MlFlow:

- `kubectl apply -k .`

>Port Forwarding: `kubectl port-forward service/mlflow-service 5000:5000 -n dev`

