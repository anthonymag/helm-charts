# helm-charts
Helm charts consumed by ArgoCD

### To package a new version

Make sure the chart is well-formed

```
helm lint [chart name]
```

From within the chart:

```
helm dep up
```

From the repository root:

```
helm package [chart name]
```

Update the `index.html`

```
helm repo index --url https://anthonymag.github.io/charts .
```

Confirm

```
cat index.html
```

