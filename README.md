
#Reference Implementation Helm Chart for HISP

This is helm chart for Reference Implementation (v8).

## 1. What is HISP?

A Health Information Service Provider, or HISP, is an accredited network service operator that enables nationwide clinical data exchange .

## 2. What is the Reference Implementation Helm Chart

A chart is package composed of files that describe a related set of [Kubernetes](http://kubernetes.io) resources. The packages
stand in a [Helm](https://helm.sh) repository. This Git repository is a Helm repository too. 

Helm packages can have dependencies much like Debian packages can have dependencies, and they greatly 
simplify the management of complex distributed systems in Kubernetes.

This chart contains definition for different services which is based on DirectProject .

## 3. Prerequisites

- Kubernetes 19+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure
- locally build docker images for each service 

## 4. Installing the Chart

To install the chart with the release name `ri8-test` just:

```bash
helm install --name ri8-test .
```

The command deploys Reference Implementation on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists the parameters that can be configured during installation.

By default all values that are specified in values.yaml file are used.

> **Tip**: List all releases using `helm list`

After the install some information should have appear in the console. If you missed it and want to check it out again try:

```bash
helm status ri8-test
```

## 5. Uninstalling the Chart

To uninstall/delete the `ri8-test` deployment:

```bash
helm delete ri8-test
```
The command removes all the Kubernetes components associated with the chart and deletes the release.
