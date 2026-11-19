# dapr-helm-charts

[Dapr](https://dapr.io/) is a portable, event-driven runtime for building distributed applications, and this repository hosts its published Helm charts at <https://dapr.github.io/helm-charts/>.

## Install Dapr on Kubernetes

Add the Helm repository and install the `dapr` chart into the `dapr-system` namespace:

```bash
helm repo add dapr https://dapr.github.io/helm-charts/
helm repo update
helm upgrade --install dapr dapr/dapr --namespace dapr-system --create-namespace
```

To list the chart versions you can install, run `helm search repo dapr --devel --versions`, then pass the one you want with `--version`.

For prerequisites, high availability, upgrades and other options, see the [Kubernetes deployment guide](https://docs.dapr.io/operations/hosting/kubernetes/kubernetes-deploy/).

## Charts

| Chart | Description |
|-------|-------------|
| `dapr` | The Dapr control plane. Source in [dapr/dapr](https://github.com/dapr/dapr/tree/master/charts/dapr), configuration reference in the [chart README](https://github.com/dapr/dapr/blob/master/charts/dapr/README.md), and listed on [Artifact Hub](https://artifacthub.io/packages/helm/dapr/dapr). |
| `dapr-dashboard` | The Dapr dashboard. Deprecated, see the note below. |

> **Note:** The `dapr-dashboard` chart is deprecated. The upstream [dapr/dashboard](https://github.com/dapr/dashboard) repository has been archived and the chart will no longer receive updates.

## Get help

If you have questions you can visit the [Dapr Documentation](https://docs.dapr.io/) or our [Discord Channel](https://discord.com/invite/ptHhX6jc34).
