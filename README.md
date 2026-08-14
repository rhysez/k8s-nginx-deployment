# k8s-nginx-deployment

This is an NGINX K8S deployment with the following:
* Assigned 'demo' namespace
* 3 replicas
* CPU and memory requests/limits
* ResourceQuota for the cluster itself
* Liveness probing after a period of 2 seconds, every 5 seconds.
* Persistent volume storage at `data/`.

This is also an experimental/exploratory K8S project for the purpose of learning the Kubernete's core components such as:
* Pods
* Nodes
* Clusters
* ResourceQuotas
* Secrets
* Volumes and Claims
* ConfigMaps
* Deployments
* Namespaces

In this project you'll find a collection of manifests grouped by their `kind`.