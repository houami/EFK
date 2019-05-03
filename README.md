Clone the repository

helm install --dry-run EFK/
(Pre-Reqs: Helm and Tiller should be running)

brew install kubernetes-helm

kubectl -n kube-system create serviceaccount tiller

kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller



kubectl port-forward <es-pod> 9200:9200 --namespace=efk
kubectl port-forward <kibana-pod> 5601:5601 --namespace=efk
