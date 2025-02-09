## Why we need service in k8s
Suppose you have done the deployment which is having 2 reploca set and it'll create the pods which is defined in the replica and a unique IP address will be assigned to each of the pods
but what happens when one of the pods got deleted? will the user able to access it via old IP? No right? Because a new replica will be created with new IP and the user will not be able to access with old IP so here we need the concept of service.

Service will run on top of Deployment and will take care of all the pods IP address since we'll creating svc file where we'll be defining labels & selectors.

## Services in Kubernetes
1. Load balencing
2. Service Discovery
3. Exposing to external world

Services mode type -
a. Cluster IP : It allows access to those only who has access to kubernetes cluster.
b. NodePort IP : It allows access to those who's access to vpc, cluster, instances
c. Load Balancer : It'll be accessiable by everyone who is having internet (Can be accessiable by anyone)
