# Scaling Kubernetes Deployments

## Manual
* As load increases on your application, you can manually increase the number of pod replicas in your deployment. Replicas are managed by a ReplicaSet. Something that we did in the Lab3.

## Horizontal Pod Autoscaler
* Horizontal Pod Autoscaler automatically scales the numbers of pods in a deployment or replica set based on observed CPU utilization.
* Scales the number of pod replicas
* kind: HorizontalPodAutoscaler

## Vertical Pod Autoscaler
* Increase CPU or memory to existing pods.
* kind: VerticalPodAutoscaler

