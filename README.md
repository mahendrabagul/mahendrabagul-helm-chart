# mahendrabagul-helm-chart
Helm chart customized to use mahendrabagul/mahendrabagul-github-client docker image. Once installed, spring boot project will be started on container in pod. The spring boot app fetches mahendrabagul's info from github api

### Helm 2
helm install https://github.com/mahendrabagul/mahendrabagul-helm-chart/releases/download/0.1.0/mahendrabagul-helm-chart-0.1.0.tgz --set service.type=NodePort

### Helm 3
helm install mahendrabagul-helm-chart https://github.com/mahendrabagul/mahendrabagul-helm-chart/releases/download/0.1.0/mahendrabagul-helm-chart-0.1.0.tgz --set service.type=NodePort

NOTES:
1. Get the application URL by running these commands:
  export NODE_PORT=$(kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services dealing-boxer-mahendrabagul-helm-chart)
  export NODE_IP=$(kubectl get nodes --namespace default -o jsonpath="{.items[0].status.addresses[0].address}")
  echo http://$NODE_IP:$NODE_PORT
