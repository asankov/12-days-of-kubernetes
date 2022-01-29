# Day 3. Kubernetes For The VI Admin

Based on <https://www.youtube.com/watch?v=uj2OcFj62ZM>.

Containers are doing to operating systems what Virtual Machines did to server hardware but with a quicker adoption cycle.

## Application Progression

Monolith -> Microservices

Containers are the construct.

Kubernetes **abstracts** infrastructure.

## Kubernetes Control Plane

Responsible for all the management work of the cluster.

### API Server

The entrypoint of Kubernetes. Users interact with the API server only.

### Controller Manager

Responsible for running the reconciliation loop and making sure that the actual state matches the desired state.

### Scheduler

Responsible for watching the API server for new pods and scheduling them.

### etcd

Database.
Responsible for storing the desired state of the cluster.

## Kubernetes Workers

Does all the work.
Communicates with the API server all the time.

### Container runtime

Responsible for running the pods.

### Kubelet

Issues command to the container runtime to create pods.

### Kube proxy

Sends packages across the overlay Kubernetes network.

## IT Challenges Today

Managing fragmented infrastructure across multiple clouds.

This is where **Tanzu Kubernetes Grid** comes in.

## Tanzu Kubernetes Grid

Run Kubernetes everywhere.

ON any infrastructure.

IN vSphere 7, AWS and VMware Cloud on AWS out-of-the-box.

AS A SERVICE with Tanzu Mission Control.

### TKG Management Cluster

Small Kubernetes cluster that runs more Kubernetes clusters.

New Kubernetes Clusters are created via CRDs.

Achievable via [Cluster API](https://github.com/kubernetes-sigs/cluster-api).

User interacts with TKS via TKG CLI/UI.

### Common Kubernetes Services that come with each cluster

#### Container Registry

Harbor - <https://goharbor.io/>

#### Ingress

Contour - <https://projectcontour.io/>

#### Logging

Fluentbit - <https://fluentbit.io/>

#### Cluster lifecycle

kubeadm - <https://github.com/kubernetes/kubeadm>

### idP Auth

dex - <https://dexidp.io/docs/kubernetes/>