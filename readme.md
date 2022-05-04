## Jupyter Lab installation on k8s

If you need a storage class and/or a persistent-volume...
```
kubectl apply -f 0-local-storage.yaml && \
mkdir -p /data && \
chmod 777 /data && \
kubectl apply -f 1-local-pv.yaml
```

Install J Lab...
```bash
kubectl create namespace jlab
kubectl apply -f 2-jupyterlab-pvc.yaml
kubectl apply -f 3-jupyterlab-deployment.yaml
kubectl apply -f 4-jupyterlab-service.yaml
```

Jupyter Lab is now provided via nodePort on [http://0.0.0.0:30888](http://0.0.0.0:30888)

⛵