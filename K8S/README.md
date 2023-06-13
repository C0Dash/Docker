# Basic Commands -
kubectl cluster-info - To get the details of kubernetes cluster
kubectl get nodes - Lists cluster nodes
kubectl get ns - List namespace
kubectl run nginx --image=nginx

Kubernetes Architecture -

![image](https://github.com/C0Dash/Docker-K8S/assets/7123309/f323b691-ef69-436e-b9a6-0b6628a03d5a)

Control plane - 
The API Server exposes a REST interface to the Kuberenetes cluster. All operations against pods, services, and so forth, are executes programmatically 
by communicating with the endpoints provided by it.

etcd is a distributed key-value store that kubernetes uses to share information about the overall state of a cluster.

