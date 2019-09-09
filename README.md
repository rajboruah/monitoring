
#Installing the helm charts:


helm install --name prometheus monitoring/prometheus --set pushgateway.persistentVolume.enabled=false --set alertmanager.persistentVolume.enabled=false --set server.persistentVolume.enabled=false
helm install --name grafana monitoring/grafana  --set service.type=NodePort

#Uninstalling the helm charts
helm delete --purge prometheus
helm delete --purge grafana
