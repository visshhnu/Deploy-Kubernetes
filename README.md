# k8s-demo
Kubernetes manifests to run the docker-hello Flask app in a cluster.

## Apply manifests
Ensure the image `docker-hello:latest` is available to the cluster (push to registry or use kind load)

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

## Debug tips
- `kubectl get pods -o wide`
- `kubectl logs deploy/hello-deploy`
- Check readiness/liveness probe failures in pod events