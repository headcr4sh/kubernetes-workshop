# Kubernetes Nodes

## Aufgaben

### 1. Zeige die aktuellen Nodes im Cluster an

```sh
kubectl get nodes
kubectl get nodes -o wide
```

### 2. Zeige eine einzelne Node im Cluster an

```sh
kubectl get nodes/${NODENAME}
```

### 3. Probiere die verschiedenen Outputs (-o) aus

```sh
kubectl get nodes/${NODENAME} -o yaml
# ... json? wide? go-template??
```