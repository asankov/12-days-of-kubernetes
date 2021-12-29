# Day 1. Kubernetes in 5 Minutes

[Kubernetes](https://kubernetes.io/), also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

## Main components

### Control plane nodes

The Control Plane nodes are resposible for running Kubernetes. They expose an API, which is used to communicate with the cluster. 

### Worker nodes

The worker nodes are responsible for running the workloads. They consists of:

- container runtime (Docker, containerd, cri-o)
- kubelet (for communicating with the control plane nodes)

## How it works

The desired state of the system is feeded to the Kube API server.
Kubernetes is then responsible for getting the actual state of the system to match the desired state.

For example, if we create a Deployment with 3 pods, Kubernetes will run the pods.
If we lose a node and some of the pods get destroyed as well, Kubernetes is resposible for rescheduling them on the other nods.
