# datashare-deploy

## Install
```sh
git clone https://github.com/PublicI/datashare-deploy.git
cd datashare-deploy
helm install --name datashare --namespace datashare ./charts/datashare/ --set basedomain=<your domain>
# import data
kubectl cp . "datashare/"$(kubectl get pod -l app=datashare-datashare --namespace=datashare -o jsonpath="{.items[0].metadata.name}")":/data"
```
