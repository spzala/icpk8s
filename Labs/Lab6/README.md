# Lab6 - some useful basic commands for troubleshooting.

## Overview
This lab answers questions like,
* What's the version of my kubernetes?
* How can I look for help?
* How do I debug?
* Run these commands and check out the output.

## Find out version
`kubectl version`

## Find out all commands
`kubectl help`

## Find out specifics about commands e.g. find out what is 'create' about.`
`kubectl create --help`

## Check the state of the resources and other details e.g. describe a pod
`kubectl describe pods <podname>`

## Look at the log of a specific pod
`kubectl logs <podname like guestbook-deployment-431080787-07lwl>`

## Check service endpoints
`kubectl get endpoints <servicename>`

## Find out details of cluster nodes
`kubectl get nodes -o yaml`

## Get status and other information about all the resources
`kubectl get events`


## Outcome of Lab6
In this lab we learn about some of commands to get useful information about Kubernetes cluster and its resources.

# Proceed to Lab7: [Lab7](../Lab7/README.md)
