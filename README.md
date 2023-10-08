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
* Terraform:
  * [How to GitOps Your Terraform](https://fluxcd.io/blog/2022/09/how-to-gitops-your-terraform/)
  * [Weave GitOps Terraform Controller - GitHub](https://github.com/weaveworks/tf-controller)
  * [Weave GitOps Terraform Controller - documentation](https://weaveworks.github.io/tf-controller/)
  * [An AWS IAM Policy Example for TF controller](https://github.com/tf-controller/aws-iam-policies)
  * [TF-controller demo: GitOps EKS nodegroup](https://github.com/tf-controller/eks-scaling)
  * [Flux provider](https://registry.terraform.io/providers/fluxcd/flux/latest)
  * [Kind provider](https://registry.terraform.io/providers/tehcyx/kind/latest)
* GitOps & Calico:
  * [GitOps and Admission Control for Calico Network Policy](https://medium.com/@bikramgupta/in-part-1-of-gitops-series-we-reviewed-the-need-for-using-gitops-for-calico-policies-and-how-to-660aa6b5e4c9)
  * [Enable GitOps for Kubernetes Security – Part 1](https://www.tigera.io/blog/enable-gitops-for-kubernetes-security-part-1/)
  * [Decentralized Calico Network Security Policy Deployment for GitOps – Part 2](https://www.tigera.io/blog/decentralized-calico-network-security-policy-deployment-for-gitops-part-2-2/)

## Solution

### Prepare local environment with Kubernetes cluster

```
cat > multi-node-k8s-no-cni.yaml <<EOF
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
networking:
  disableDefaultCNI: true
  podSubnet: 192.168.0.0/16
EOF

kind create cluster --config multi-node-k8s-no-cni.yaml --name home-lab

kubectl get nodes -o wide

kind get clusters

kind delete cluster -n home-lab
```

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
