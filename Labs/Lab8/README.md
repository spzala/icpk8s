# Lab8 - shows how to pass env variables to container.

## Pre-req: Make sure you are in the Lab8 directory

## Overview:
Set an environment variable for your container.

## Deploy pod
`kubectl create -f env-variable.yaml`

## Verify that env variable is passed to your container
`kubectl exec nginx -- printenv`


## Outcome of Lab8
In this lab we learn how to pass env variable to container in a pod.
