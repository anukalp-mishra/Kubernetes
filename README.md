# Kubernetes
Everything about k8s
## K8’s Architecture -
 
![Controllers](https://github.com/user-attachments/assets/153f3903-daa5-40dd-aadf-2010e1063121)
Control Plane (Master Node)
API Server
Basic: The core component of Kubernetes that handles all incoming requests.
Advanced: It serves as a gateway to the Kubernetes cluster, validating and configuring data for the API objects which include pods, services, replication controllers, and others.
etcd
Basic: A key-value store that holds all the cluster-related information.
Advanced: It stores configuration data, state data, and metadata about the cluster, ensuring consistency and reliability for distributed systems.
Scheduler
Basic: Responsible for scheduling pods or resources on the cluster.
Advanced: It watches for newly created pods with no assigned node and selects a node for them based on resource requirements and policies.
Controller Manager
Basic: Ensures that the controllers, like replica sets, are running as expected.
Advanced: It combines several controller functions into a single process to reduce complexity, managing operations such as node lifecycle, endpoints, and namespace management.
Cloud Controller Manager
Basic: Manages interactions with cloud providers, similar to Terraform.
Advanced: It abstracts cloud-specific control logic, allowing Kubernetes to interact with the cloud provider’s API to manage resources like virtual machines, load balancers, and storage.
Data Plane (Worker Node)
Kubelet
Basic: Creates and ensures that pods are always running on the node.
Advanced: It manages the lifecycle of containers, ensuring they are healthy and running as expected, and integrates with container runtimes like Docker or containerd.
Kube Proxy
Basic: Provides networking capabilities and default load balancing for services.
Advanced: It maintains network rules on nodes, allowing network communication to your pods from network sessions inside or outside of your cluster.
Container Runtime
Basic: Runs containers inside pods.
Advanced: It is the software responsible for running the containers, with popular options being Docker, containerd, and CRI-O, ensuring containers are launched, running, and isolated properly.
