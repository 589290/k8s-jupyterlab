## Jupyter Lab installation on k8s
```bash
kubectl apply -f jupyterlab-pvc.yaml
kubectl apply -f jupyterlab-deployment.yaml
kubectl apply -f jupyterlab-service.yaml
```
