# Scaling Kubernetes Deployments

## Manual
* As load increases on your application, you can manually increase the number of pod replicas in your deployment. Replicas are managed by a ReplicaSet. Something that we are doing in this Lab3.

## Horizontal Pod Autoscaler
* Horizontal Pod Autoscaler automatically scales the numbers of pods in a deployment or replica set based on observed CPU utilization.
* Scales the number of pod replicas.
* `kind: HorizontalPodAutoscaler`
* Supported at the beta level.

## Vertical Pod Autoscaler
* Increase CPU or memory to existing pods.
* It can both down-scale pods that are over-requesting resources, and also up-scale pods that are under-requesting resources based on their usage over time.
* `kind: VerticalPodAutoscaler`
* Supported at the beta level.

