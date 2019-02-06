# Lab3 - Scale your app  

## Overview:
Kubernetes deployment can easily be scaled using ReplicaSet.

## Go to Lab3 directory
The directory has guestbook-deployment.yaml.yaml file in there.
It's the same file that we had used in previous lab except that we have changed the replica to 3.

`cd ~/icpk8s/Labs/Lab3`

## Scale to 3 pods i.e. application load can now be divided between three pods.

`kubectl apply -f guestbook-deployment.yaml`

## Guestbook deployment should have three pods now

`kubectl get pods -l app=guestbook`


##  Outcome of Lab3
In this lab we have scaled existing deployment of guestbook to 3 pods for high availability.
