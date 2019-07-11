# datashare-deploy

## Install
```sh
https://github.com/PublicI/datashare-deploy.git
helm install --name datashare --namespace datashare ./charts/datashare/
# import data
kubectl cp . "datashare/"$(kubectl get pod -l app=datashare-datashare --namespace=datashare -o jsonpath="{.items[0].metadata.name}")":/data"
```
