# Kubernetes Namespaces

## Aufgaben

### 1. Erstelle einen neuen Namespace

```sh
kubectl create namespace my-namespace
```

### 2. Schaue Dir den neuen Namespace an

```sh
kubectl get namespaces | grep my-namespace

kubectl describe namespaces/my-namespace
kubectl describe namespace/my-namespace
kubectl describe namespace my-namespace
kubectl describe ns my-namespace

kubectl get namespaces/my-namespace -o yaml | less

```

### 3. Editiere den Namespace

```sh
kubectl edit namespaces/my-namespace
```

### 4. Lösche den neuen Namespace

```sh
kubectl delete namespaces/my-namespace
```

### 5. Erstelle, editiere und lösche einen Namespace deklarativ

Nutze hierzu die Datei `playround.yaml` in Verbindung mit `kubectl [...] -f`
