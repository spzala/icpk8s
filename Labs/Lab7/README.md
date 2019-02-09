# Lab7 - Deploy guestbook with Helm

## Overview:
Helm is a package manager for Kubernetes. It's easy to create and deploy helm charts.
In our previous exercise we deployed nginx directly with the Kuberntes. In this exercise,
we will do the same but using helm chart.

## Clean up
Let's remove earlier deployments of guestbook we created with using `kubectl`:

`kubectl delete deployments guestbook-v1 redis-master redis-slave`

`kubectl delete svc guestbook redis-master redis-slave`

## Install helm

Helm needs to be installed in this virtual machine.

Run the following commands to install it:

```bash
cd ~
curl -kLo helm-linux-amd64-v2.9.1.tar.gz https://icp1-master.patrocinio.org:8443/api/cli/helm-linux-amd64.tar.gz
tar xzvf helm-linux-amd64-v2.9.1.tar.gz
sudo mv linux-amd64/helm /usr/local/bin
```
(the ibmuser password is `thinkibm`)

## Check existing installation of Helm chart
`helm ls --tls`

## Initialize Helm repositories
`helm init --client-only`

## Check what Helm repositories you have
`helm repo list`

## Add helm101 repo
`helm repo add helm101 https://ibm.github.io/helm101/`

## Verify that helm101/guestbook is now in your repo
`helm repo list`

`helm search helm101`

## Install guestbook
`helm install helm101/guestbook --name guestbook<firstandlastname> --set serviceType=NodePort --tls`

## Access the application

Run the following command to retrieve the NodePort number:

`kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services guestbook<firstandlastname>-guestbook`

You will see a port number (like 31753)

Open your browser to `http://icp1-proxy.patrocinio.org:<port-number>`

## Check chart release history
`helm history guestbook<firstandlastname> --tls`

## Clean up
First remove the repo:
`helm repo remove helm101`
Delete all Kubernetes resources generated when the chart was instantiated:
`helm delete --purge guestbook<firstandlastname> --tls`


## Outcome of Lab7
In this lab we got a basic understanding of Helm and deployed guestbook application using Helm chart.


# Proceed to Lab8: [Lab8](../Lab8/README.md)
