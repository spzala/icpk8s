# Lab10 - shows how to create and use Secret.

## Pre-req: Make sure you are in the Lab10 directory

## Overview:
Create secret. There are multiple ways to use secret in your app, this exercise shows the usage of secret via env variables.


## Generate encoded user name and password
`echo -n 'user-testapp' | base64
Example output of the command: dXNlci10ZXN0YXBw) 

`echo -n 'passw0rd$blu123' | base64`
Example output of the command: cGFzc3cwcmQkYmx1MTIz

## Create secret. Modify the secret.yaml with your values from above two steps.
`kubectl create -f secret.yaml`

## Verify secret
`kubectl get secret secret-excercise`

## Use secret in a pod
`kubectl create -f secret-env-variable.yaml`

## Verify that secret was retrieved
`kubectl exec sec-nginx -- printenv`
Output of the command should have SEC_USER=user-testapp and SEC_PASSWORD=passw0rd$blu123 along with other env variables

## Outcome of Lab10
In this lab we learn how to create and use secret.