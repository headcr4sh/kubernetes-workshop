# Kubernetes ConfigMaps und Secrets

## Gruppenübungen

### 1. Lege die ConfigMap und das Secret an

```sh
kubectl apply -f ./mariadb-config.yaml
kubectl apply -f ./mariadb-secrets.yaml
```

### 2. Schaue Dir die Inhalte von ConfigMap und Secret an

```sh
kubectl get configmap/mariadb -o yaml
kubectl get secret/mariadb -o yaml

kubectl get secret/mariadb -o go-template='{{range $k,$v := .data}}{{"### "}}{{$k}}{{"\n"}}{{$v|base64decode}}{{"\n\n"}}{{end}}'
```

### 3. Schaue Dir das mariadb Pod manifest an und aktiviere es in Deinem Cluster

```sh
kubectl apply -f ./mariadb-pod.yaml
```

## Fragen

### 1. Kann man ausser einfachen Key-Value-Paaren auch ganze "Datein" in ConfigMaps speichern?

## Abschliessendes

### Lösche den Pod, die ConfigMap und das Secret wieder

```
kubectl delete -f ./mariadb-config.yaml
kubectl delete -f ./mariadb-secrets.yaml
kubectl delete -f ./mariadb-pod.yaml
```