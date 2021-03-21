## Prerequsite

* Minikube v1.6.2 or greater with ingress plugin enabled

* Helm 3.2.3 or greater

## Questions

1. What is Kubernetes and what is it for?
  Kubernetes is an open-source container orchestration platform that enables the operation of an elastic web server framework for cloud applications
  This platform to schedule and run containers on clusters of physical or virtual machines, control and automate application deployments, scale containerized applications and their resources

2. What Kubernetes entities can you list and what is their purpose?
  - Pod represents a process running in your cluster; it also represents a single instance of an application running in your cluster
  - ReplicaSet is a group of identical Pods that are running
  - Namespace - to divide cluster resources
  - Deployments - provides ability to update applications
  - Secret - stores secrets
  - Service - used to expose application to be able to communicate a different set of pods between each other
  - DaemonSet - ensures that all / some eligible nodes run a copy of a Pod

3. What tools did you use to work with Kubernetes and what tasks did you solve?
  Unfortunately I have never used Kubernetes

4. What is helm chart?
  helm charts are Kubernetes YAML manifests combined into a single package that can be advertised to your Kubernetes clusters

5. What is an umbrella chart?
  umbrella chart may have multiple subcharts, each of which functions as a piece of the whole


## Tasks

* create helm charts for applications from [docker-compose](../03%20-%20docker-compose) task

* create an umbrella helm chart for you helm charts

* `*` Lint and deploy the umbrella helm chart

* `*` Deploy logging and monitoring tools for your users
