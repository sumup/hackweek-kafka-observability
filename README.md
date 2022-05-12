##### Run Below commands
kubectl apply -f k8s/kafka-secrets.yaml
kubectl apply -f k8s/prometheus-config.yaml 
kubectl apply -f k8s/prometheus-deployment.yaml
kubectl apply -f k8s/prometheus-service.yaml
kubectl apply -f k8s/grafana-deployment.yaml
kubectl apply -f k8s/grafana-service.yaml

##### Port Forward
kubectl port-forward service/prometheus-service 8090:9090 

kubectl port-forward service/grafana-service 3000:3000 
