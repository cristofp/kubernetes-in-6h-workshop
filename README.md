# Workshop Info

This repository contains materials for workshop "Start using Kubernetes as Developer in 6h".

Atendees are asked to bring their own laptops with prepared environment according to instructions enclosed in section below.
Basic familiarity with Docker and containerization is expected.

This repository will be updated with further materials on workshop day.

## Local envorionment setup

### 1. Setup connection to some kubernetes cluster with kubectl
You can do this by:
  * Installing locally minikube [instructions](https://kubernetes.io/docs/tasks/tools/install-minikube/)
  * Buying kubernetes cluster subscription on one of cloud providers (e.g. [azure](https://azure.microsoft.com/en-us/free/kubernetes-service/), [google cloud](https://cloud.google.com/kubernetes-engine/), [aws](https://aws.amazon.com/kubernetes/) ) and configuring connection to remote cluster according to instructions provided provider's page
   
Verify that the setup is correct, by running in console:
```
kubectl cluster-info
```
   
You should get similar output:
```
Kubernetes master is running at https://172.17.85.7:8443
KubeDNS is running at https://172.17.85.7:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
```
   
### 2. Install docker
Install docker on your local machine accoring to instructions on [docker page](https://docs.docker.com/install/)
 


## Feedback
I'd be very grateful for you feedback after workshop: https://forms.gle/dS9JGCF2kdfgYevs9
