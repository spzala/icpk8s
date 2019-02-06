# Set up connection to Kubernetes environment

We need to establish connection to a Kubernetes environment.

In this lab, we will use IBM Cloud Private (ICP), hosted in IBM Cloud.

Follow these steps to configure your connection to ICP:

* Open a Terminal window

* Go to the directory `icp-health`

```
cd icp-health
```

* Update this github repository to latest version:

```
git pull
```

* Run the following command to establish the connection:

```
./configureHelmCLI.sh icp1-master.patrocinio.org
```

and type the following information:


| Field | Value |
|---|---|
| Username | admin |
| Password | admin |
| namespace | 2 (default) |

* You can now validate your connection by running the following command:

```
kubectl cluster-info
```

# Proceed to Lab1: [Lab1](../Lab1/README.md)
