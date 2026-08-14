# k8s-nginx-deployment

This is an NGINX K8S deployment with the following:
* Assigned 'demo' namespace
* 3 replicas
* CPU and memory requests/limits
* ResourceQuota for the cluster itself
* Liveness probing after a period of 2 seconds, every 5 seconds.
* Persistent volume storage at `data/`.

There are also a couple of other manifests that target this deployment via the `app: nginx` label:
1. The service `manifests/services/demo-service-for-nginx.yaml` can be applied to expose this deployment to the rest of the cluster.
2. The network policy `manifests/networkpolicy/simple-network-policy.yml` can be applied to forcibly disallow ingress/egress from all pods in the cluster, but allow it for pods with the `app: nginx` label (this deployment).

This is also an experimental/exploratory K8S project for the purpose of learning the Kubernete's core components such as:
* Pod
* Node
* Cluster
* ResourceQuota
* Secret
* PersistentVolume & PersistentVolumeClaim
* ConfigMap
* Deployment
* Namespace
* Service
* NetworkPolicy

In this project you'll find a collection of manifests grouped by their `kind`.