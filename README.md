# Decision service

## Kubernetes (deploy on cluster)

### `docker build -t jtutzo/katawolf/decisionservice .`

Build app and docker image

### `kubectl apply -f ./k8s-manifests`

Deploy on kubernetes cluster

### `kubectl delete -f ./k8s-manifests`

Delete on kubernetes cluster
