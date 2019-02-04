# Lab5 - Access the guestbook app

## Pre-req: Make sure you are in the Lab5 directory.

## Overview:
Let's expose the service so it can be accessed via internet. Ideally before exposing a
service to outside you should secure it but for quick lab purpose of testing we will go without
securing. Kubernetes supports two primary modes of finding a Service - environment variables and DNS. 

## Check your service via DNS
`kubectl get services guestbook --namespace=<nameofyournamespace>`

## Grep nodeport
`kubectl get svc guestbook -o yaml | grep nodePort`

## Access the service using node IP and NodePort
Run `http://10.0.0.3:<nodePort> (e.g. http://10.0.0.3:32583)`
(OR `$http://localhost:<nodePort>`)
Since our proxy IP is http://10.0.0.3 so we can access the service externally via browser as above.
You can also `curl <nodeIP>:<nodePort> (e.g. curl http://192.168.99.100:32583  OR curl http://10.0.0.3:32583))`


## Output:
By end of the Lab5, we accessed the guestbook application and played with it.


#NOTE: outside the lab, you can also set your NodePort and IP as below, and access service: 
* `export NODE_PORT=$(kubectl get --namespace <nameofyournamespace> -o jsonpath="{.spec.ports[0].nodePort}" services guestbook)`
* `export NODE_IP=$( kubectl get nodes --namespace <nameofyournamespace> -o jsonpath="{.items[0].status.addresses[0].address}")`
* `curl http://$NODE_IP:$NODE_PORT`





