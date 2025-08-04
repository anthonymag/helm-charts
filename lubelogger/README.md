## secrets to create

### lubelogger-creds

```yaml
apiVersion: v1
data:
  MailConfig__EmailFrom: replaceme_base64
  MailConfig__EmailServer: replaceme_base64
  MailConfig__Password: replaceme_base64
  MailConfig__Port: replaceme_base64
  MailConfig__Username: replaceme_base64
kind: Secret
metadata:
  annotations:
  name: lubelogger-creds
  namespace: lubelogger
type: Opaque
```

### lubelogger-postgres-connection

```yaml
apiVersion: v1
data:
  POSTGRES_CONNECTION: replaceme_base64
kind: Secret
metadata:
  annotations:
  name: lubelogger-postgres-connection
  namespace: lubelogger
type: Opaque
```
