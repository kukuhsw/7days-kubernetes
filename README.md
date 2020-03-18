## 🚀&nbsp; List of Kubernetes Command

Kubernetes is a platform for managing containerized workloads. Kubernetes orchestrates computing, networking and storage to provide a seamless portability across infrastructure providers.

### Viewing Resource Information

Nodes:
```shell
kubectl get no
kubectl get no -o wide
kubectl describe no
kubectl get no-o yaml
kubectl get node --selector=[label_name]
kubectl get nodes -o jsonpath='{.items[*].status.addresses[?(@.type=="ExternalIP")].address}'
kubectl top node [node_name]
```

Pods:
```shell
kubectl get po
kubectl get po -o wide
kubectl describe po
kubectl get po --show-labels
kubectl get po -l app=nginx
kubectl get po-o yaml
kubectl get pod [pod_name] -o yaml --export
kubectl get pod [pod_name] -o yaml --export > nameoffile.yaml
kubectl get pods --field-selector status.phase=Running
```

Namespaces:
```shell
kubectl get ns
kubectl get ns -o yaml
kubectl describe ns
```

Deployment:
```shell
kubectl get deploy
kubectl describe deploy
kubectl get deploy -o wide
kubectl get deploy -o yaml
```

Services:
```shell
kubectl get svc
kubectl describe svc
kubectl get svc -o wide
kubectl get svc -o yaml
kubectl get svc --show-labels
```

Logs:
```shell
kubectl logs [pod_name]
kubectl logs --since=1h [pod_name]
kubectl logs --tail=20 [pod_name]
kubectl logs -f -c [container_name] [pod_name]
kubectl logs [pod_name] > pod.log
```

ReplicaSets:
```shell
kubectl get rs
kubectl describe rs
kubectl get rs -o wide
kubectl get rs -o yaml
```