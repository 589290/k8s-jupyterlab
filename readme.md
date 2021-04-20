## Jupyter Lab installation on k8s
```bash
kubectl apply -f jupyterlab-pvc.yaml
kubectl apply -f jupyterlab-deployment.yaml
kubectl apply -f jupyterlab-service.yaml
```
  
If deployed on minikube locally, use...
```bash
minikube tunnel
```
...to expose the service on [http://0.0.0.0:8888](http://0.0.0.0:8888)
