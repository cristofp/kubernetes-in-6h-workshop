# Workshop Info

This repository contains materials for workshop "Start using Kubernetes as Developer in 6h".

Workshop is dedicated to software developers with no or little knowledge about Kubernetes. However, basic familiarity with containerization and Docker is expected.

Atendees are asked to bring their own laptops with prepared environment according to instructions enclosed in section below.

## Local envorionment setup

### 1. Setup connection to some kubernetes cluster with kubectl
You can do this by:
  * Installing locally minikube [instructions](https://kubernetes.io/docs/tasks/tools/install-minikube/)
  * Buying kubernetes cluster subscription on one of cloud providers (e.g. [azure](https://azure.microsoft.com/en-us/free/kubernetes-service/), [google cloud](https://cloud.google.com/kubernetes-engine/), [aws](https://aws.amazon.com/kubernetes/) ) and configuring connection to remote cluster according to instructions provided provider's page
   
Verify that the setup is correct, by 

#### A. Checking cluster connectivity
```
kubectl cluster-info
```
   
You should get similar output:
```
Kubernetes master is running at https://172.17.85.7:8443
KubeDNS is running at https://172.17.85.7:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
```
#### B. Checking connectivity from cluser to Docker Hub
 Run in console:
 ```
 kubectl run my-httpd --image=httpd --port=80 --restart=Never
 ```
 Then following command will try to download `httpd` docker image from public registry your cluster. After while, a run of following command:
 ```
 kubectl get pods
 ```
 should return output similar to:
 ```
 NAME                        READY   STATUS    RESTARTS   AGE
 my-httpd                    1/1     Running   0          24s
 ```

#### C. Checking port-forward functionality
Check if you can forward port of application running on Kubernetes to your localhost, and access it via browser.

Run in console:
```
kubectl port-forward my-httpd 9999:80
```
And then open in browser `localhost:9999`. You should get a page with "It works!" message.

 
   
### 2. Install docker
Install docker on your local machine accoring to instructions on [docker page](https://docs.docker.com/install/)
 


## Feedback
I'd be very grateful for you feedback after workshop: https://forms.gle/dS9JGCF2kdfgYevs9
