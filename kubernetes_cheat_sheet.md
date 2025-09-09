# Kubernetes Commands Cheat Sheet

This guide provides a summary of common Kubernetes commands for managing your cluster and applications.

## Cluster Management

- `kubectl cluster-info`: Display information about the master and services in the cluster.
- `kubectl version`: Display the Kubernetes version running on the client and server.
- `kubectl config view`: Get the cluster's configuration.
- `kubectl config get-contexts`: Display a list of contexts.
- `kubectl config current-context`: Display the current context.
- `kubectl config use-context <cluster_name>`: Set the default context.
- `kubectl api-resources`: List the available API resources.
- `kubectl api-versions`: List the available API versions.

## Nodes

- `kubectl get nodes`: List one or more nodes.
- `kubectl delete node <node_name>`: Delete a node or multiple nodes.
- `kubectl top node <node_name>`: Display resource usage (CPU/Memory/Storage) for nodes.
- `kubectl annotate node <node_name>`: Annotate a node.
- `kubectl cordon node <node_name>`: Mark a node as unschedulable.
- `kubectl uncordon node <node_name>`: Mark a node as schedulable.
- `kubectl drain node <node_name>`: Drain a node in preparation for maintenance.
- `kubectl label node`: Add or update the labels of one or more nodes.
- `kubectl taint node <node_name>`: Update the taints on one or more nodes.

## Pods

- `kubectl get pod`: List one or more pods.
- `kubectl get pods --sort-by='.status.containerStatuses[0].restartCount'`: List pods sorted by restart count.
- `kubectl get pods --field-selector=status.phase=Running`: Get all running pods in the namespace.
- `kubectl delete pod <pod_name>`: Delete a pod.
- `kubectl describe pod <pod_name>`: Display the detailed state of a pod.
- `kubectl create pod <pod_name>`: Create a pod.
- `kubectl exec -it <pod_name> /bin/sh`: Get an interactive shell on a single-container pod.
- `kubectl top pod`: Display resource usage (CPU/Memory/Storage) for pods.
- `kubectl annotate pod <pod_name> <annotation>`: Add or update the annotations of a pod.
- `kubectl label pods <pod_name> new-label=<label_name>`: Add or update the label of a pod.
- `kubectl get pods --show-labels`: Get pods and show labels.
- `kubectl port-forward <pod_name> <port_to_listen_on>:<port_to_forward_to>`: Listen on a local port and forward to a port on a specified pod.

## Namespaces

- `kubectl create namespace <namespace_name>`: Create a namespace.
- `kubectl get namespace <namespace_name>`: List one or more namespaces.
- `kubectl describe namespace <namespace_name>`: Display the detailed state of one or more namespaces.
- `kubectl delete namespace <namespace_name>`: Delete a namespace.
- `kubectl edit namespace <namespace_name>`: Edit and update the definition of a namespace.
- `kubectl top namespace <namespace_name>`: Display resource usage (CPU/Memory/Storage) for a namespace.

## Deployments

- `kubectl get deployment`: List one or more deployments.
- `kubectl delete deployment <deployment_name>`: Delete a deployment.
- `kubectl describe deployment <deployment_name>`: Show the details of a deployment.
- `kubectl create deployment <deployment_name> --image=<image_name>`: Create a new deployment.
- `kubectl scale deployment <deployment_name> --replicas=<number>`: Scale a deployment to the specified number of replicas.
- `kubectl set image deployment/<deployment_name> <container_name>=<new_image>`: Update the image of a container in a deployment.
- `kubectl rollout undo deployment/<deployment_name>`: Roll back a deployment to the previous version.

## Services

- `kubectl get services`: List all services.
- `kubectl expose deployment <deployment_name> --port=<port> --target-port=<target-port>`: Expose a deployment as a new service.
- `kubectl delete service <service_name>`: Delete a service.
- `kubectl describe service <service_name>`: Show the details of a service.

## Events

- `kubectl get events`: List recent events for all resources in the system.
- `kubectl get events --field-selector type=Warning`: List warnings only.
- `kubectl get events --sort-by=.metadata.creationTimestamp`: List events sorted by timestamp.