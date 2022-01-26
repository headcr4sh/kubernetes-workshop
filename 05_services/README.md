# Kubernetes Services

## Gruppenübungen

### 1. Erstelle einen Pod mit einem vorgeschalteten Service

```sh
kubectl apply -f ./pod-and-service.yaml
```

### 2. Schaue Dir Service und Pod mit kubectl describe an

...

### 3. Nutze kubectl port-forward, um den Pod über den Service anzusprechen

ACHTUNG: Das funktioniert in der Praxis nicht so, wie man es erwartet!

## Fragen

### 1. Was ist der Unterschied zwischen den verschiedenen service types?

### 2. Wozu dienen die Selectors der Services?

### 3. Was passiert, wenn zwei Services die gleichen Pods selektieren?

### 4. Was passiert, wenn ein Service unterschiedliche Pods selektiert?

### 5. Wie kann man überprüfen, welche Pods ein Service selektiert?

### 6. Wie können Pods mit Hilfe von Services miteinander kommunizieren?
...