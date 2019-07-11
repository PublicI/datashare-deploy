# datashare-deploy

## Install
```sh
helm install --name datashare --namespace datashare ./charts/datashare/
```

## Import
```sh
kubectl cp . "datashare/"$(kubectl get pod -l app=datashare-datashare --namespace=datashare -o jsonpath="{.items[0].metadata.name}")":/data"
```
