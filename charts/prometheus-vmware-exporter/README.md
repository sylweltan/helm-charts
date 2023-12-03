# Prometheus Vmware Exporter

A Prometheus exporter for [VMware ESXi](https://www.vmware.com/products/esxi-and-esx.html) metrics.

This chart bootstraps a Prometheus [VMware Exporter](https://github.com/sylweltan/prometheus-vmware-exporter) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Get Helm Repository Info

```console
helm repo add sylweltan https://sylweltan.github.io/helm-charts
helm repo update
```

_See [`helm repo`](https://helm.sh/docs/helm/helm_repo/) for command documentation._

## Install Chart

```console
helm install [RELEASE_NAME] sylweltan/prometheus-vmware-exporter
```

_See [configuration](#configuration) below._

_See [helm install](https://helm.sh/docs/helm/helm_install/) for command documentation._

## Uninstall Chart

```console
helm uninstall [RELEASE_NAME]
```

This removes all the Kubernetes components associated with the chart and deletes the release.

_See [helm uninstall](https://helm.sh/docs/helm/helm_uninstall/) for command documentation._

_See [helm upgrade](https://helm.sh/docs/helm/helm_upgrade/) for command documentation._

## Upgrading Chart

```console
helm upgrade [RELEASE_NAME] [CHART] --install
```

### Version 0.1.0

prometheus-vmware-exported has been set to [v1.0.5](https://github.com/sylweltan/prometheus-vmware-exporter/releases/tag/v1.0.5).

## Configuration

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing). To see all configurable options with detailed comments, visit the chart's [values.yaml](https://github.com/sylweltan/helm-charts/blob/main/charts/prometheus-vmware-exporter/values.yaml), or run these configuration commands:

```console
helm show values sylweltan/prometheus-vmware-exporter
```

### VMware ESXi Connection

The exporter connects to VMware ESXi using API.

- To configure VMware connection by value, set `vmware.username`, `vmware.password`, `vmware.host` and `vmware.log`
- To configure VMware connection by existing secret, you must store above connection variables in a secret, and set `vmware.existingSecret` to `[SECRET_NAME]`

### Exporter Documentation and Params

Documentation for the VMware Exporter can be found here: (<https://github.com/sylweltan/prometheus-vmware-exporter>)

### Collector Flags

Available collector flags can be found in the [values.yaml](https://github.com/sylweltan/helm-charts/blob/main/charts/prometheus-vmware-exporter/values.yaml) and a description of each flag can be found in the [prometheus-vmware-exporter](https://github.com/sylweltan/prometheus-vmware-exporter) repository.
