#### Clone the repository

> https://github.com/houami/EFK.git

#### Helm Install

> helm install --name EFK --dry-run EFK/

#### Accessing the application

> kubectl port-forward <es-pod> 9200:9200 --namespace=efk
> kubectl port-forward <kibana-pod> 5601:5601 --namespace=efk


#### Pre-Reqs:
##### Helm and Tiller should be running
Helm version : v2.13.1

##### Installing Helm Client
```
brew install kubernetes-helm
```

##### Installing Tiller

```

kubectl -n kube-system create serviceaccount tiller

kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller

helm init --service-account tiller
```


