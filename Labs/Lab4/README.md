# Lab4 - Services

## Pre-req: Make sure you are in the Lab3 directory.

## Overview:
A Service is an abstraction which defines a logical set of Pods running in your cluster, 
that all provide the same functionality. 
When created, each Service is assigned a unique IP address, which is tied to the lifespan of the Service,
and will not change while the Service is alive. 

## Let's first check out what we have
`kubectl get pods -l app= guestbook -o wide`

## Check pods IP
`kubectl get pods -l app= guestbook -o yaml | grep podIP`

## Create the Redis master service
`kubectl create -f redis-master-service.yaml`

## Create the Redis slave service
`kubectl create -f redis-slave-service.yaml`

## Create the guestbook service
`kubectl create -f guestbook-service.yaml`

## Check all services 
`kubectl get svc guestbook`

## Check pods endpoints
`kubectl describe svc guestbook`

## Outcome of Lab4
In this lab we accomplished following,
1. Created service for guestbook, redis master and redis slave deployment
2. Accessed service from a node within the cluster.
