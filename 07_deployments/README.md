# Kubernetes Deployments

## Gemeinsame übungen

### 1. Schaut Euch die Datei mariadb.yaml an und applied sie im Cluster

```sh
kubectl apply -f ./mariadb.yaml
```

### 2. Schaut Euch die Logs des mariadb containers an

```sh
kubectl logs -f -l app.kubernetes.io/name=wordpress-mariadb
```

### Gruppenübungen

### 1. Repariert den Container und sorgt dafür, dass die Datenbank ordentlich startet.

Die Dokumentation des Containers ist hier: https://hub.docker.com/_/mariadb

### 2. Sorgt dafür, dass beim Starten des Conainers automatisch eine Datenbank-Definition geladen wird

Der Ordner `/docker-entrypoint-initdb.d` im Container muss hierzu mindestens eine Datei (z.B. mit der Endung `.sql`)
beinhalten. Diese Datei könnte z.B. so aussehen:

```sql
CREATE TABLE foo (bar varchar(16), baz varchar(16));
```

*Hinweis:* Nutzt hierzu `spec.template.spec.volumets` und `spec.template.spec.containers[0].volumeMounts` in Verbindung
mit einem Merhzeiligen Eintrag in einer ConfigMap.
