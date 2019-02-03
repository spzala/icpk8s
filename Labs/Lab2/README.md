# Lab2 - Deployment

## Pre-req: Make sure you are in the Lab2 directory.

## Overview:
Deployment is an abstractions on pods and replica set.

## Create the Redis master deployment
`kubectl create -f redis-master-deployment.yaml`

### Check the status of what you just deployed
`kubectl get deploy`

## Create the Redis slave deployment
`kubectl create -f redis-slave-deployment.yaml`

## Create the guestbook deployment
`kubectl create -f guestbook-deployment.yaml`

## Check the status of all deployments
`kubectl get deployments`

## Display information about a specific deployment

`kubectl describe deployment guestbook-deployment`

## List the pods created by the deployment

`kubectl get pods -l app=guestbook`

## Display information about a specific pod

`kubectl describe pod <pod-name>`
 
(where `<pod-name>` is the name of one of your pod. For example, `kubectl describe pod guestbook-deployment-431080787-gj435`) 

## Check logs of a pod

`kubectl logs <pod-name>`

(where `<pod-name>` is the name of one of your pod. For example, `kubectl logs guestbook-deployment-431080787-gj435`)


## Outcome of Lab2:
In this lab we accomplished the following,
1. Deployed guestbook application and Redis database into Kubernetes by using Kubernetes resource Deployment. 
2. Verified deployment and looked into a pod that was created with the deployment.
