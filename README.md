# datashare-deploy

[ICIJ Datashare](https://datashare.icij.org/) lets you index and search documents on your computer, and this Helm chart extends that to your very own cluster with Kubernetes and [Helm](https://helm.sh/).

_Note: unofficial chart not affiliated with ICIJ. Alpha-quality. Use at your own risk._

## Install
```sh
git clone https://github.com/PublicI/datashare-deploy.git
cd datashare-deploy
helm install --name datashare --namespace datashare ./charts/datashare/
# import data
kubectl cp . "datashare/"$(kubectl get pod -l app=datashare-datashare --namespace=datashare -o jsonpath="{.items[0].metadata.name}")":/data"
```
