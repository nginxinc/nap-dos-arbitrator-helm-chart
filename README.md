# NGINX App Protect DoS Arbitrator Helm Chart

## Introduction

This chart deploys the NGINX App Protect DoS Arbitrator in your Kubernetes cluster.

## Prerequisites

  - Helm 3.0+.

## Getting the Chart Sources

```console
$ helm pull nginx-stable/nginx-appprotect-dos-arbitrator --untar
```

## Adding the Helm Repository

This step is required if you're installing the chart via the helm repository.

```console
$ helm repo add nginx-stable https://helm.nginx.com/stable
$ helm repo update
```

## Installing the Chart

### Installing via Helm Repository

To install the chart with the release name my-release-dos (my-release-dos is the name that you choose):

```console
$ helm install my-release-dos nginx-stable/nginx-appprotect-dos-arbitrator
```

### Installing Using Chart Sources

To install the chart with the release name my-release-dos (my-release-dos is the name that you choose):

```console
$ helm install my-release-dos .
```

The command deploys the App Protect DoS Arbitrator in your Kubernetes cluster in the default configuration. The configuration section lists the parameters that can be configured during installation.

## Upgrading the Chart

### Upgrading the Release

To upgrade the release `my-release-dos`:

#### Upgrade Using Chart Sources:

```console
$ helm upgrade my-release-dos .
```

#### Upgrade via Helm Repository:

```console
$ helm upgrade my-release-dos nginx-stable/nginx-appprotect-dos-arbitrator
```

## Uninstalling the Chart

### Uninstalling the Release

To uninstall/delete the release `my-release-dos`:

```console
$ helm uninstall my-release-dos
```

The command removes all the Kubernetes components associated with the release and deletes the release.

## Configuration

The following tables lists the configurable parameters of the NGINX App Protect DoS Arbitrator chart and their default values.

Parameter | Description | Default
--- | --- | ---
`resources` | The resources of the Arbitrator pods. | limits:<br>cpu: 500m<br>memory: 128Mi
`image.repository` | The image repository of the Arbitrator image. | docker-registry.nginx.com/nap-dos/app_protect_dos_arb
`image.tag` | The tag of the Arbitrator image. | 1.1.0
`image.pullPolicy` | The pull policy for the Arbitrator image. | IfNotPresent
