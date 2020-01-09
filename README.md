# mahendrabagul-helm-chart
Helm chart customized to use mahendrabagul/mahendrabagul-github-client docker image. Once installed, spring boot project will be started on container in pod. The spring boot app fetches mahendrabagul's info from github api

helm install https://github.com/mahendrabagul/mahendrabagul-helm-chart/releases/download/0.1.0/mahendrabagul-helm-chart-0.1.0.tgz --set service.type=NodePort


