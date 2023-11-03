# KubernetesPOC
To Overview on Kubernetes

What is it ? ->

What is pod ? ->

what does pod do ? ->

How containers with in a pod communicate ? -> 

what is Kubernetes cluster ? -> 

Difference in Kubernetes and Docker ? ->

when to use docker vs docker compose vs docker swarm vs kubernetes ? ->

Pod usage patterns ? ->

Benefits of pod ? ->

Statefulset in kubernetes ? ->

How to rollback a Deployment ? ->

what happens when a master fails & worker fails ?->

what are namespaces ? ->


Create a Namespace
The following command is used to create a namespace.

apiVersion: v1
kind: Namespce
metadata
   name: elk



Features of Kubernetes
Following are some of the important features of Kubernetes.

Continues development, integration and deployment

Containerized infrastructure

Application-centric management

Auto-scalable infrastructure

Environment consistency across development testing and production

Loosely coupled infrastructure, where each component can act as a separate unit

Higher density of resource utilization

Predictable infrastructure which is going to be created


Kubernetes - Master Machine Components
Following are the components of Kubernetes Master Machine.

etcd
It stores the configuration information which can be used by each of the nodes in the cluster. It is a high availability key value store that can be distributed among multiple nodes. It is accessible only by Kubernetes API server as it may have some sensitive information. It is a distributed key value Store which is accessible to all.

API Server
Kubernetes is an API server which provides all the operation on cluster using the API. API server implements an interface, which means different tools and libraries can readily communicate with it. Kubeconfig is a package along with the server side tools that can be used for communication. It exposes Kubernetes API.

Controller Manager
This component is responsible for most of the collectors that regulates the state of cluster and performs a task. In general, it can be considered as a daemon which runs in nonterminating loop and is responsible for collecting and sending information to API server. It works toward getting the shared state of cluster and then make changes to bring the current status of the server to the desired state. The key controllers are replication controller, endpoint controller, namespace controller, and service account controller. The controller manager runs different kind of controllers to handle nodes, endpoints, etc.


Scheduler
This is one of the key components of Kubernetes master. It is a service in master responsible for distributing the workload. It is responsible for tracking utilization of working load on cluster nodes and then placing the workload on which resources are available and accept the workload. In other words, this is the mechanism responsible for allocating pods to available nodes. The scheduler is responsible for workload utilization and allocating pod to new node.

Kubernetes - Node Components
Following are the key components of Node server which are necessary to communicate with Kubernetes master.

Docker
The first requirement of each node is Docker which helps in running the encapsulated application containers in a relatively isolated but lightweight operating environment.

Kubelet Service
This is a small service in each node responsible for relaying information to and from control plane service. It interacts with etcd store to read configuration details and wright values. This communicates with the master component to receive commands and work. The kubelet process then assumes responsibility for maintaining the state of work and the node server. It manages network rules, port forwarding, etc.
