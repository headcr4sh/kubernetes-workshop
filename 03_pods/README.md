# Kubernetes Pods

## Gemeinsame übungen

### 1. Erstelle einen "nginx" Pod mit Hilfe der beigelegeten YAML Datei

```sh
kubectl apply -f ./nginx.yaml
```

### 2. Schau Dir den Pod an

```sh
kubectl get pods/aufgabe03-nginx
```

### 3. Nutze port-forward, um einen HTTP-Request gegen den Pod abzusetzen

```sh
LOCAL_PORT=8080 # Setze diese Variable entsprechend Deinem Gusto. ;-)
kubectl port-forward pods/aufgabe03-nginx ${LOCAL_PORT}:80

# Neues Fenster / oder nimm einen Browser, wenn Dir eine GUI lieber ist!
curl http://localhost:${LOCAL_PORT}
```

### Gruppenübungen

### 1. Füge explizite "port"-Konfiguration in die Pod spec ein!

(Im YAML unter `spec.containers[0].ports`)

### 2. Nutze einen versionierten Tag für das Container Image (nicht latest!)

### 3. Nutze eine SHA256 Checksum für das Container Image anstatt eines Tags

### 4. Setze eine imagePullPolicy für den Container


## Fragen

### 1. In welchem Namespace wurde der Pod erstellt?

Analysiere hierzu die Ausgabe von `kubectl describe pods/aufgabe03-nginx`.

### 2. Wie kannst Du den Namespace in dem der Pod erstellt wird, ändern?

## Abschluss

### 1. Lösche alle nginx Pods in allen Namespaces, die Du angelegt hat.

```sh
kubectl get pods --all-namespaces
kubectl get pods -A
```