# argocd-applications

### nginx-ingress
[Azure Ingress Documentation](https://docs.microsoft.com/en-us/azure/aks/ingress-basic?tabs=azure-cli)

```shell
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
helm template ingress-nginx/ingress-nginx --namespace ingress-nginx --version 4.0.13 --create-namespace > ingress-nginx-4.0.13.yaml
#helm pull ingress-nginx/ingress-nginx --untar
```

### cert-manager
[Cert Manager Documentation](https://cert-manager.io/docs/installation/helm/#steps)

```shell
helm repo add https://charts.jetstack.io
helm repo update
helm template jetstack/cert-manager --namespace cert-manager --version v1.8.0 --set installCRDs=true > cert-manager-v1.8.0.yaml
```