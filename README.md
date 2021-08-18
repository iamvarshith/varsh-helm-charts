# TOC 
- [Helm charts installation](#helm-installation)
    * [Helm defaults used with the chart](#helm-defaults-used-with-the-chart)

# Helm installation

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:
```sh
helm repo add kubetest-helm-charts https://kubeshop.github.io/helm-charts
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
kubetest-helm-charts` to see the charts.

To install the kubetest chart:
```sh
helm install my-<chart-name> kubetest-helm-charts/kubetest
```
To uninstall the kubetest chart:
```sh
helm delete my-<chart-name> kubetest-helm-charts/kubetest
```
> Please note that this Helm chart will install all the needed charts. Including CRDs. It's an umbrella chart.
