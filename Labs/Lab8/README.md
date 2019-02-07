# Lab8 - shows how to pass env variables to container.

## Overview:
Set an environment variable for your container.

## Go to Lab8 directory
cd ~/icpk8s/Labs/Lab8`

## Deploy pod
`kubectl create -f env-variable.yaml`

## Verify that env variable is passed to your container
`kubectl exec nginx -- printenv`


## Outcome of Lab8
In this lab we learn how to pass env variable to container in a pod.

# Proceed to Lab9: [Lab9](../Lab9/README.md)
