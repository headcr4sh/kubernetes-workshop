# Kubernetes Labels und Annotations

## Gemeinsame Übungen

### 1. Erstelle die beiden Pods, die in nginx-pods.yaml definiert sind

```sh
kubectl apply -f ./nginx-pods.yaml
```

### 2. Schaue Dir die Labels der Pods an

```sh
kubectl get pods --show-labels
```

### 3. Lass Dir Pods anhand von ausgesuchten Labels anzeigen

Nutze hierzu `kubectl get -l`

```sh
kubectl get pods -l 
```

## Fragen

### 1. Wozu sind Labels und Annotations gut?

## Abschliessendes

### 1. Lösche die beiden Pods wieder aus Deinem Cluster

```sh
kubectl delete -f ./nginx-pods.yaml
```