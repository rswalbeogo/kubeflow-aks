•	az login as SP

•	az set subscription

•	az aks get-credentials --resource-group _kubeflow-rg-01_ --name _kubeflow-test-aks-14_

•	kubelogin convert-kubeconfig -l azurecli

•	az aks update -n _kubeflow-test-aks-14_ -g _kubeflow-rg-01_ --attach-acr _kubeflowacr01_

•	cd manifests

•	while ! kustomize build tls | kubectl apply -f -; do echo "Retrying to apply resources"; sleep 10; done

•	kubectl rollout restart deployment dex -n auth

•	kubectl get services -n istio-system istio-ingressgateway -o yaml

•	**_>> input the ip address displayed from above command into certificate file in deployment/tls and manifest/tls_**

•	kubectl apply -f _~/kubeflow_091723/kubeflow-aks/manifests/tls/certificate.yaml_

•	kubectl apply -f _~/kubeflow_091723/kubeflow-aks/deployments/tls/certificate.yaml_

•	**_>> input ip address in web browser_**

•	Email address: user@example.com

•	Password : 12341234

=====================================================================================

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](./CONTRIBUTING.md)
![current development version](https://img.shields.io/badge/Kubeflow-v1.6.1-green)
[![License](https://img.shields.io/github/license/azure/kubeflow-aks)](./LICENSE)

This is not an officially supported Microsoft product. This project is actively being maintained.

# Kubeflow on Azure Kubernetes Service

The Kubeflow project is dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable. Our goal is not to recreate other services, but to provide a straightforward way to deploy best-of-breed open-source systems for ML on Azure Kubernetes Services.

## Getting Started

There are a number of deployment options for running Kubeflow on AKS. To get started with deploying Kubeflow on [Azure Kubernetes Service](https://learn.microsoft.com/en-us/azure/aks/intro-kubernetes), see the [deployment options section](https://azure.github.io/kubeflow-aks/main/docs/deployment-options/) on the [Kubeflow on AKS](https://azure.github.io/kubeflow-aks/main) website.

## Help & Feedback

For help, please consider the following venues (in order):

* [Documentation](https://azure.github.io/kubeflow-aks/main/docs)
* [Search open issues](https://github.com/Azure/kubeflow-aks/issues)
* [File an issue](https://github.com/Azure/kubeflow-aks/issues/new)

## Contributing

We welcome community contributions and pull requests.

See our [contribution guide](./CONTRIBUTING.md) for more information on how to
report issues, set up a development environment, and submit code.

We adhere to the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).

## Security

See [SECURITY](./SECURITY.md) for more information.

## License

This project is [licensed](./LICENSE) under the  MIT License.

