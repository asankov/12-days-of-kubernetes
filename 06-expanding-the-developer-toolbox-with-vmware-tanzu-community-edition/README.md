# Day 6. Expanding the Developer Toolbox with VMware Tanzu Community Edition

This day is about this blog post: <https://tanzu.vmware.com/developer/blog/expanding-the-developer-toolbox-with-vmware-tanzu-community-edition/>

It mentions few useful tools to use along with Kubernetes/VMware Tanzu Community Edition:

## [Spring](https://spring.io/)

Web framework for Java application.

## Buildpacks

[Cloud Native Buildpacks](https://buildpacks.io/) enable building a container image from source code without the need for a Dockerfile.

Tools like [kpack](https://github.com/pivotal/kpack) ease the process of building container images by extending Kubernetes.

This can be combined with [skaffold](https://skaffold.dev/docs/pipeline-stages/builders/buildpacks/) for even better developer experience.

## [Carvel](https://carvel.dev/)

Carvel provides a set of reliable, single-purpose, composable tools that aid in your application building, configuration, and deployment to Kubernetes.

## [KubeApps](https://kubeapps.com/)

KubeApps is a dashboard for Tanzu that surfaces and presents Bitnami Application Catalog to the users.

It allows you to install tools like databases, caches, etc. into your cluster with just one click.
