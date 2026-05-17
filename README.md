# Travelo Flight Booking

Travelo is a React + Spring Boot + MySQL application.

## DevOps assignment files

- `k8s/base/`: required Kubernetes manifests for the `travelo` namespace.
- `k8s/monitoring/`: Prometheus, Grafana, Loki and Promtail configuration for observability.
- `k8s/helm/travelo/`: optional Helm chart bonus.
- `k8s/gitops/`: optional Argo CD GitOps example.
- `skaffold.yaml`: optional Skaffold development workflow.
- `docs/MANUAL_STEPS.md`: exact local setup and deployment commands.
- `docs/REPORT_DRAFT.md`: report-ready explanation of the work.
- `docs/SCREENSHOT_CHECKLIST.md`: screenshots to capture for the PDF.
- `rapport.pdf`: final PDF report with screenshots.
- `rapport.tex`: LaTeX source of the final report.

Start with:

```bash
kubectl apply -k k8s/base
```

For the full guided workflow, follow `docs/MANUAL_STEPS.md`.
