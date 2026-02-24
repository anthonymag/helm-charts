Until I have a secret manager, manually create secrets:

```yaml
apiVersion: v1
data:
  nextcloud-password: changemebase64
  nextcloud-username: changemebase64
  smtp-host: changemebase64
  smtp-password: changemebase64
  smtp-username: changemebase64
kind: Secret
metadata:
  name: nextcloud
  namespace: nextcloud
type: Opaque
---
apiVersion: v1
data:
  db-password: changemebase64
  db-username: changemebase64
  db-hostname: changemebase64
  db-name: changemebase64
kind: Secret
metadata:
  annotations:
  name: nextcloud-db
  namespace: nextcloud
type: Opaque
---
apiVersion: v1
data:
  redis-password: changemebase64
kind: Secret
metadata:
  name: nextcloud-cache
  namespace: nextcloud
type: Opaque
```

