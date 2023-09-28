# Kubernetes networking automation using GitOps

## Idea

Practice GitOps approach to manage network settings in Kubernetes cluster deployed locally.

## Tools

* [kind](https://kind.sigs.k8s.io/)
  * [Kind multi-node](https://docs.tigera.io/calico/latest/getting-started/kubernetes/kind)
  * [Kind quickstart](https://kind.sigs.k8s.io/docs/user/quick-start/)
  * [Kind networking](https://kind.sigs.k8s.io/docs/user/configuration/#networking)
* [Kustomize](https://kustomize.io/)
* [Calico](https://docs.tigera.io/calico/latest/getting-started/kubernetes/)
  * [Networking](https://docs.tigera.io/calico/latest/networking/)
  * [Security](https://docs.tigera.io/calico/latest/network-policy/)
* [Flux](https://fluxcd.io/)
  * [Ways of structuring your repositories](https://fluxcd.io/flux/guides/repository-structure/)
  * [Flux bootstrap](https://fluxcd.io/flux/installation/bootstrap/)
  * [``flux bootstrap github``](https://fluxcd.io/flux/cmd/flux_bootstrap_github/)
  * [``flux check``](https://fluxcd.io/flux/cmd/flux_check/)
  * [Manage Helm Releases](https://fluxcd.io/flux/guides/helmreleases/)
  * [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack)
* [Flagger](https://flagger.app/)
  * [Flagger Install with Flux](https://docs.flagger.app/install/flagger-install-with-flux)
  * [Flagger Install on Kubernetes](https://docs.flagger.app/install/flagger-install-on-kubernetes)
  * [NGINX Canary Deployments](https://docs.flagger.app/tutorials/nginx-progressive-delivery)
  * [Deployment Strategies](https://docs.flagger.app/usage/deployment-strategies)
  * [Canary deployment](https://docs.flagger.app/usage/how-it-works#canary-resource)
  * [Canary analysis with Prometheus Operator](https://docs.flagger.app/tutorials/prometheus-operator)
* Sample Cloud Native applications:
  * [Project pod tato Head](https://github.com/podtato-head/podtato-head)
  * [Podinfo](https://github.com/stefanprodan/podinfo)

## Solution

### Prepare local environment with Kubernetes cluster

TODO:

### Configure basic networking settings

TODO:

### Prepare Flux to GitOps approach

TODO:

### Deploy demo application

TODO:

### Prepare Flagger for progressive delivery

TODO:

### Use Kustomize to define Calico network policies

TODO:
