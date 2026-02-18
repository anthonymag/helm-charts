Prerequisite secret:

```yaml
apiVersion: v1
data:
  db-hostname: replacemebase64
  db-password: replacemebase64
  db-username: replacemebase64
kind: Secret
metadata:
  name: immich-db
  namespace: immich
type: Opaque
```
