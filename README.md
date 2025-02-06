# Kubernetes
Everything about k8s
## K8’s Architecture -
 
![Controllers](https://github.com/user-attachments/assets/153f3903-daa5-40dd-aadf-2010e1063121)
## Control plane (master node)
1. api server - core component of k8s, accepts all incoming  reqs, exposes k8s to external world.
2. etcd - key value store, cluster related infos.
3. scheduler - scheduling pods or resources on k8s, receives info from api server & acts on it
4. controller manager - ensures controllers like replica set are running
5. cloud controller manager - like terraform

## Data plane (worker node)
1. kubelet - creates pod, ensures pod is always running
2. kube proxy - provides networking like Docker0, default load balancing
3. container runtime - runs container inside pod
