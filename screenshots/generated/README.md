# Generated Kubernetes Evidence

- `01-minikube-status.svg`: `minikube status`
- `02-kubectl-nodes.svg`: `kubectl get nodes -o wide`
- `03-namespace.svg`: `kubectl get ns travelo`
- `04-pods-wide.svg`: `kubectl get pods -n travelo -o wide`
- `05-workloads-services-ingress-pdb.svg`: `kubectl get deploy,statefulset,svc,ingress,pdb -n travelo`
- `06-configmaps-secrets.svg`: `kubectl get configmap,secret -n travelo`
- `07-resource-quota.svg`: `kubectl describe quota travelo-resource-quota -n travelo`
- `08-rbac-can-read.svg`: `kubectl auth can-i get pods --as=system:serviceaccount:travelo:travelo-deployer -n travelo`
- `09-rbac-cannot-delete.svg`: `kubectl auth can-i delete pods --as=system:serviceaccount:travelo:travelo-deployer -n travelo`
- `10-ingress.svg`: `kubectl describe ingress travelo-ingress -n travelo`
- `11-backend-logs.svg`: `kubectl logs -n travelo deploy/backend --tail=50`
- `12-top-nodes.svg`: `kubectl top nodes`
- `13-top-pods.svg`: `kubectl top pods -n travelo`
- `14-backend-probes.svg`: `kubectl describe deployment backend -n travelo`
- `15-frontend-probes.svg`: `kubectl describe deployment frontend -n travelo`
- `16-mysql-probes.svg`: `kubectl describe pod mysql-0 -n travelo`
- `17-frontend-http-access.svg`: `curl -I http://127.0.0.1:18080`
- `18-backend-http-access.svg`: `curl http://127.0.0.1:18081/api/hello`
- `19-monitoring-pods.svg`: `kubectl get pods -n monitoring`
- `20-helm-monitoring-releases.svg`: `helm list -n monitoring`
- `21-servicemonitor.svg`: `kubectl get servicemonitor -n monitoring`
- `22-grafana-dashboard-configmap.svg`: `kubectl get configmap travelo-dashboard -n monitoring`
- `23-loki-datasource-configmap.svg`: `kubectl get configmap loki-datasource -n monitoring`
- `24-loki-promtail.svg`: `kubectl get statefulset,daemonset,svc -n monitoring`

## Browser Screenshots

- `30-frontend-browser.png`: Travelo frontend served from the Kubernetes frontend service through port-forward.
- `31-backend-browser.png`: Backend `/api/hello` endpoint served from the Kubernetes backend service through port-forward.
- `33-grafana-dashboards-authenticated.png`: Authenticated Grafana dashboard list.
- `34-grafana-travelo-dashboard.png`: Travelo Grafana dashboard with CPU, memory, restart and Loki log panels.
- `35-grafana-explore-logs.png`: Authenticated Grafana Explore page.
