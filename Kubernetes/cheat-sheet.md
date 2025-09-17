# 📌 Kubectl Cheatsheet

---

## Cluster Info
```bash
kubectl version                  # Show client & server versions
kubectl cluster-info             # Show cluster details
kubectl get nodes                # List all nodes in the cluster
kubectl describe node <node>     # Get detailed info about a node
```

## Namespaces
```bash
kubectl get namespaces                              # List namespaces
kubectl config set-context --current --namespace=<ns>   # Switch default namespace
kubectl create namespace dev                        # Create new namespace
kubectl delete namespace dev                        # Delete namespace
```

## Pods
```bash
kubectl run mypod --image=nginx:latest        # Create a pod
kubectl get pods                              # List pods
kubectl get pods -o wide                      # Show pods with node info & IP
kubectl describe pod mypod                    # Detailed info about pod
kubectl logs mypod                            # Show logs from pod
kubectl logs -f mypod                         # Stream logs (like tail -f)
kubectl exec -it mypod -- /bin/bash           # Open shell inside container
kubectl delete pod mypod                      # Delete pod
```

## Deployments
```bash
kubectl create deployment myapp --image=nginx:latest        # Create deployment
kubectl get deployments                                     # List deployments
kubectl describe deployment myapp                           # Details of deployment
kubectl scale deployment myapp --replicas=3                 # Scale replicas
kubectl set image deployment/myapp nginx=nginx:1.19         # Update image
kubectl rollout status deployment/myapp                     # Check rollout progress
kubectl rollout undo deployment/myapp                       # Rollback to previous version
kubectl delete deployment myapp                             # Delete deployment
```

## Services
```bash
kubectl expose pod mypod --type=NodePort --port=80               # Expose a pod
kubectl expose deployment myapp --type=ClusterIP --port=8080     # Expose deployment
kubectl get svc                                                  # List services
kubectl describe svc myapp                                       # Detailed service info
kubectl delete svc myapp                                         # Delete service
```

## Config & Secrets
```bash
kubectl create configmap myconfig --from-literal=key=value         # Create configmap
kubectl create configmap myconfig --from-file=config.txt           # From file
kubectl get configmaps                                             # List configmaps
kubectl describe configmap myconfig                                # View details

kubectl create secret generic mysecret --from-literal=user=admin   # Create secret
kubectl get secrets                                                # List secrets
kubectl describe secret mysecret                                   # Describe secret
```

## Debugging
```bash
kubectl describe pod <pod>               # Events + status of pod
kubectl logs <pod>                       # Pod logs
kubectl logs <pod> -c <container>        # Logs from specific container
kubectl exec -it <pod> -- /bin/bash      # Exec into pod
kubectl get events --sort-by=.metadata.creationTimestamp  # Show recent events
```

## Apply & Delete Manifests
```bash
kubectl apply -f pod.yaml                 # Apply manifest
kubectl apply -f deployment.yaml          # Apply deployment
kubectl apply -f .                        # Apply all manifests in directory
kubectl delete -f pod.yaml                # Delete resource from manifest
kubectl delete all --all                  # Delete everything in current namespace
```

## Resource Exploration
```bash
kubectl get all                      # Get all resources in namespace
kubectl api-resources                 # List all supported resource types
kubectl explain pod                   # Show API docs for a resource
kubectl explain pod.spec.containers   # Drill down into fields
```

## Shortcuts (Aliases)
```bash
kubectl get pods → kubectl get po
kubectl get services → kubectl get svc
kubectl get deployments → kubectl get deploy
kubectl get namespaces → kubectl get ns
```

## Pro Tip
Add this alias to your shell config (~/.bashrc or ~/.zshrc) for less typing:
```bash
alias k=kubectl
```
Then just use:
```bash
k get pods
k describe pod mypod
```
