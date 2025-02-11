# Kubernetes
Everything about k8s
## K8’s Architecture -
 
![Controllers](https://github.com/user-attachments/assets/153f3903-daa5-40dd-aadf-2010e1063121)

## Control Plane (Master Node)
<li>API Server</li>
<ul>The core component of Kubernetes that handles all incoming requests.</ul>
<ul>It serves as a gateway to the Kubernetes cluster, validating and configuring data for the API objects which include pods, services, replication controllers, and others.</ul>
<li>etcd</li>
<ul>A key-value store that holds all the cluster-related information.</ul>
<ul>It stores configuration data, state data, and metadata about the cluster, ensuring consistency and reliability for distributed systems.</ul>
<li>Scheduler</li>
<ul>Responsible for scheduling pods or resources on the cluster.</ul>
<ul>It watches for newly created pods with no assigned node and selects a node for them based on resource requirements and policies.</ul>
<li>Controller Manager</li>
<ul>Ensures that the controllers, like replica sets, are running as expected.</ul>
<ul>It combines several controller functions into a single process to reduce complexity, managing operations such as node lifecycle, endpoints, and namespace management.</ul>
<li>Cloud Controller Manager</li>
<ul>Manages interactions with cloud providers, similar to Terraform.</ul>
<ul>It abstracts cloud-specific control logic, allowing Kubernetes to interact with the cloud provider’s API to manage resources like virtual machines, load balancers, and storage.</ul>
## Data Plane (Worker Node)
<li>Kubelet</li>
<ol>Creates and ensures that pods are always running on the node.</ol>
<ol>It manages the lifecycle of containers, ensuring they are healthy and running as expected, and integrates with container runtimes like Docker or containerd.</ol>
<li>Kube Proxy</li>
<ol>Provides networking capabilities and default load balancing for services.</ol>
<ol>It maintains network rules on nodes, allowing network communication to your pods from network sessions inside or outside of your cluster.</ol>
<li>Container Runtime</li>
<ol>Runs containers inside pods.</ol>
<ol>It is the software responsible for running the containers, with popular options being Docker, containerd, and CRI-O, ensuring containers are launched, running, and isolated properly.</ol>
