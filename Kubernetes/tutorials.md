# Kubernetes Tutorials

This file takes you from **beginner to advanced** in Kubernetes.

---

## Beginner Tutorials
### 1. Setup Kubernetes Locally
- Option 1: [Minikube](https://minikube.sigs.k8s.io/docs/start/) (runs K8s locally with a VM/driver).
- Option 2: [Kind](https://kind.sigs.k8s.io/) (Kubernetes in Docker).

Verify installation:
```bash
kubectl version --client
minikube start
```

### 2. Run Your First Pod
```bash
kubectl run nginx --image=nginx --port=80
kubectl get pods
```
Pod → The smallest deployable unit in Kubernetes, usually wrapping one container.

### Expose Your Pod with a Service
```bash
kubectl expose pod nginx --type=NodePort --port=80
kubectl get services
```
Service → Lets other apps (or users) talk to your Pod.

## Intermediate Tutorials
### 1. Deployments
```bash
kubectl create deployment hello --image=gcr.io/google-samples/hello-app:1.0
kubectl get deployments
kubectl scale deployment hello --replicas=3
```
Deployment → Manages Pods for high availability and scaling.

### Rolling Updates
```bash
kubectl set image deployment/hello hello=gcr.io/google-samples/hello-app:2.0
kubectl rollout status deployment/hello
```
### Namespaces
```bash
kubectl create namespace dev
kubectl get pods --namespace=dev
```
Namespace → Logical isolation for resources.

## Advanced Tutorials
- Setup Ingress Controller for HTTP routing.
- Configure Liveness & Readiness probes.
- Use Persistent Volumes for databases.
- Apply RBAC (Role-Based Access Control).
- Deploy monitoring stack with Prometheus & Grafana.
