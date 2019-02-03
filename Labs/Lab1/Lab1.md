# Instructions for Lab1, create namespace and context

## Pre-req: you have a Kubernetes cluster created. Also, make sure you are in the Lab1 directory.

## Overview:
Kubernetes supports multiple virtual clusters backed by the same physical cluster. 
These virtual clusters are called namespaces.
Kubernetes namespaces help different projects, teams, or customers to share a Kubernetes cluster.
A Kubernetes namespace provides the scope for Pods, Deployments and Services in the cluster.

## Create namespace

```kubectl create namespace think```

## Verify namespace

`kubectl get namespaces`

## create and set context 

kubectl config set-context test --cluster mycluster.icp --user admin --namespace <firstandlastnamewithmiddleinitial>

kubectl config set current-context test

## get contexts

kubectl config get-contexts

## display current context

$kubectl config current-context



## Outcome of Lab1:
In this lab we accomplished following,
1. Created specific namespace
2. Created context
3. Set current context to what we have created
So now our following labs will have it's own namespace (aka virtual cluster) and context.
