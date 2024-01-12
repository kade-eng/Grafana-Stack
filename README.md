# Grafana-Stack Helm CHart

This Helm chart deploys a comprehensive monitoring stack, including Grafana, Tempo, Loki, Promtail, Prometheus, and Thanos. It simplifies the setup process by automatically adding Tempo, Loki, and Prometheus datasources to Grafana.

## Prerequiresites
- Kubernetes cluster
- Kubectl tool
- Helm version 3.x

## Installation
1. ```git clone https://github.com/kade-eng/grafana-stack.git```
2. ```cd grafana-stack```
3. ```helm dependency build```
4. ```helm install grafana-stack ./ --namespace monitoring```

## Accessing Grafana
You can quickly access grafana for testing purposes by port-forwarding the grafana-stack service (ex. ```kubectl port-forward svc/grafana-stack 3000:80```) and then viewing from localhost (ex. ```http://localhost:3000/```)

## Additional Information
More information on how to configure each chart can be found on the source chart GitHub pages:

https://github.com/grafana/helm-charts/tree/main/charts

https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus

## Contributing
Contributions are welcome via GitHub pull requests.
