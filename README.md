# helm-charts
Helm charts consumed by ArgoCD

### To package a new version

Make sure the chart is well-formed

```
helm lint [chart name]
```

From within the chart (TODO: confirm necessity):

```
helm dep up
```

From the repository root:

```
helm package [chart name]
```

Get the remote index

```
wget https://raw.githubusercontent.com/anthonymag/helm-charts/refs/heads/main/index.yaml
```

Update the `index.html`

```
helm repo index --url https://github.com/anthonymag/helm-charts/releases/download --merge index.yaml .
```

Confirm

```
cat index.html
```


