# Lab1 - Namespace and Context

<!--
## Pre-req: you have a Kubernetes cluster created. Also, make sure you are in the Lab1 directory.
-->

## Overview:
Kubernetes supports multiple virtual clusters backed by the same physical cluster.
These virtual clusters are called namespaces.
Kubernetes namespaces help different projects, teams, or customers to share a Kubernetes cluster.
A Kubernetes namespace provides the scope for Pods, Deployments and Services in the cluster.

## Create namespace
The namespace is required to be unique among lab participant. Please user your
first and last name with middleinitial as one word to name your namespace.

`kubectl create namespace <yourfirstandlastnamewithmiddleinitial>`

## Verify namespace

`kubectl get namespaces`

## Create and Set context

`kubectl config set-context test --cluster mycluster.icp --user admin --namespace <nameofyournamespace>`

`kubectl config set current-context test`

## Get Contexts

`kubectl config get-contexts`

## Display Current Context

`kubectl config current-context`



## Outcome of Lab1:
In this lab we accomplished following,
1. Created a specific namespace to use with the rest of the labs
2. Created context
3. Set current context to the one we have created
So now our following labs will have it's own namespace (aka virtual cluster) and context.
