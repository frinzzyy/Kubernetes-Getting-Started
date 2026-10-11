# Exercise 1 — Kubernetes Hello Pod

run Nginx as `hello-k8s`, expose it with a NodePort Service, and open it via Minikube.

```bash
minikube start
kubectl apply -f k8s.yaml
kubectl get pods,services
kubectl wait --for=condition=Ready pod/hello-k8s --timeout=120s
minikube service hello-k8s
```
 Pod is `Running` and browser shows the Nginx welcome page. Cleanup: `kubectl delete -f k8s.yaml`.
