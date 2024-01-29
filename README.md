# Tolgee Helm Chart

This repository contains the Helm chart for integrating Tolgee, an open-source translation management system, into a Kubernetes cluster.

## Prerequisites

`Kubernetes 1.12+`
`Helm 3.1.0`

## Installing the Chart

To install the chart with the release name my-release:

``` bash  
helm install my-release ./tolgee
```

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```bash
helm delete my-release
```

## Configuration

The following table lists the configurable parameters of the Tolgee chart and their default values.

| Parameter | Description | Default |
| --- | --- | --- |
|image.repository|Tolgee image repository|tolgee/tolgee|
|image.tag|Tolgee image tag|latest|
|image.pullPolicy|Tolgee image pull policy|IfNotPresent|
|service.type|Kubernetes Service type|ClusterIP|
|service.port|Kubernetes Service port|80|
|ingress.enabled|Enable ingress controller resource|false|
|ingress.annotations|Ingress annotations|{}|
|ingress.hosts|Ingress hostnames|[]|
|ingress.tl|Ingress TLS configuration (YAML)|[]|

Specify each parameter using the --set key=value[,key=value] argument to helm install. For example,

``` bash
helm install my-release
--set image.tag=latest
./tolgee
```

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

``` bash
helm install my-release -f values.yaml ./tolgee
```

This README provides a brief description of the Helm chart, instructions for installing and uninstalling the chart, and a table of configurable parameters. You can customize this README to include more information about your Helm chart, such as its features, architecture, and usage examples.