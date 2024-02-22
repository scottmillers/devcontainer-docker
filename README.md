# Explore how to use Docker inside a Dev Container

While you can build, deploy, and debug your application inside a dev container, you may also need to test it by running it inside a set of production-like containers. Fortunately, by installing the needed Docker or Kubernetes CLIs and mounting your local Docker socket, you can build and deploy your app's container images from inside your dev container.

## Docker from Docker

https://github.com/microsoft/vscode-dev-containers/tree/main/containers/docker-from-docker

## Docker in Docker

https://github.com/microsoft/vscode-dev-containers/tree/main/containers/docker-in-docker

Dev containers can be useful for all types of applications including those that also deploy into a container based-environment. While you can directly build and run the application inside the dev container you create, you may also want to test it by deploying a built container image into your local Docker Desktop instance without affecting your dev container.

In many cases, the best approach to solve this problem is by bind mounting the docker socket, as demonstrated in /containers/docker-from-docker. This definition demonstrates an alternative technique called "Docker in Docker".

## Kubernetes - Minikube-in-Docker

https://github.com/microsoft/vscode-dev-containers/tree/main/containers/kubernetes-helm-minikube


## Reference

https://code.visualstudio.com/remote/advancedcontainers/use-docker-kubernetes