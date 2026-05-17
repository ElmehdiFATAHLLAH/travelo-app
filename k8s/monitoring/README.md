# Travelo Monitoring Stack

This folder contains the files used for Volet 3.

- `prometheus-values.yaml`: installs Prometheus, Grafana, Alertmanager, kube-state-metrics and node-exporter with Helm.
- `backend-servicemonitor.yaml`: tells Prometheus to scrape Spring Boot metrics from `/actuator/prometheus`.
- `loki-values.yaml`: installs Loki for log storage.
- `promtail-values.yaml`: installs Promtail so pod logs are collected and sent to Loki.
- `loki-datasource-configmap.yaml`: registers Loki as a Grafana datasource.
- `travelo-dashboard-configmap.yaml`: imports a small Travelo dashboard into Grafana.

The detailed install commands are in `docs/MANUAL_STEPS.md`.
