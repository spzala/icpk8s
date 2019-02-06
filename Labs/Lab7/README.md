# Lab7 - Deploy guestbook with Helm

## Pre-req: Helm is installed in your environment.

## Overview:
Helm is a package manager for Kubernetes. It's easy to create and deploy helm charts.
In our previous exercise we deployed nginx directly with the Kuberntes. In this exercise,
we will do the same but using helm chart.

## Clean up
Let's remove earlier deployments of guestbook we created with using `kubectl`
`kubectl delete deployments guestbook`
`kubectl delete svc guestbook`

## Check existing installation of Helm chart
`helm ls`

## Check what Helm repositories do you have
`helm repo list`

## Add helm101 repo
`helm repo add helm101 https://ibm.github.io/helm101/`

## Verify that helm101/guestbook is now in your repo
`helm repo list`
`helm search helm101`

## Install guestbook
`helm install helm101/guestbook --name myguestbook --set serviceType=NodePort`
Follow the output instructions to see your guestbook application

## Check chart release history
`helm history myguestbook`

## Clean up
First remove the repo:
`helm repo remove helm101`
Delete all Kubernetes resources generated when the chart was instantiated:
`helm delete --purge myguestbook`


## Outcome of Lab7
In this lab we got a basic understanding of Helm and deployed guestbook application using Helm chart.


# Proceed to Lab8: [Lab8](../Labs/Lab8/README.md)
