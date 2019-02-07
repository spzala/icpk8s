# Lab9 - shows how to globally set variable using ConfigMap

## Overview:
Set an environment variable in your container with ConfigMap.
ConfigMap allows many different option for creating global key-value pairs, this lab shows one of many ways
of using it.

## Go to Lab9 directory
`cd ~/icpk8s/Labs/Lab9`

## Create configmap
`kubectl create -f configmap.yaml`

## Deploy pod
`kubectl create -f configmap-env-variable.yaml`

## Verify that env variable is passed to your container
`kubectl exec cm-nginx -- printenv`

## Outcome of Lab9:
In this lab we learn how to pass env variable to container in a pod using ConfigMap.

# Proceed to Lab10: [Lab10](../Lab10/README.md)
