# Important Kubernetes Commands

## Cluster Operations

- `kubectl cluster-info`: Display information about the Kubernetes cluster.
- `kubectl get nodes`: List all the nodes in the cluster.
- `kubectl get pods --all-namespaces`: List all pods in all namespaces.
- `kubectl get namespaces`: List all namespaces in the cluster.

## Pod Operations

- `kubectl get pods`: List all pods in the current namespace.
- `kubectl describe pod <pod-name>`: Get detailed information about a specific pod.
- `kubectl logs <pod-name>`: Retrieve the logs of a specific pod.
- `kubectl exec -it <pod-name> -- <command>`: Run a command inside a specific pod.

## Deployment Operations

- `kubectl get deployments`: List all deployments in the current namespace.
- `kubectl describe deployment <deployment-name>`: Get detailed information about a specific deployment.
- `kubectl scale deployment <deployment-name> --replicas=<replica-count>`: Scale a deployment to a specific number of replicas.
- `kubectl rollout status deployment <deployment-name>`: Check the status of a deployment rollout.

## Service Operations

- `kubectl get services`: List all services in the current namespace.
- `kubectl describe service <service-name>`: Get detailed information about a specific service.
- `kubectl expose deployment <deployment-name> --port=<port> --target-port=<target-port> --type=<service-type>`: Expose a deployment as a service.

## ConfigMap and Secret Operations

- `kubectl get configmaps`: List all ConfigMaps in the current namespace.
- `kubectl describe configmap <configmap-name>`: Get detailed information about a specific ConfigMap.
- `kubectl get secrets`: List all Secrets in the current namespace.
- `kubectl describe secret <secret-name>`: Get detailed information about a specific Secret.

## Persistent Volume Operations

- `kubectl get pv`: List all PersistentVolumes in the cluster.
- `kubectl describe pv <pv-name>`: Get detailed information about a specific PersistentVolume.
- `kubectl get pvc`: List all PersistentVolumeClaims in the current namespace.
- `kubectl describe pvc <pvc-name>`: Get detailed information about a specific PersistentVolumeClaim.

> Note: Replace `<pod-name>`, `<deployment-name>`, `<service-name>`, `<configmap-name>`, `<secret-name>`, `<pv-name>`, and `<pvc-name>` with the actual names in your Kubernetes cluster.
