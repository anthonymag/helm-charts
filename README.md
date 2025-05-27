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
rm *.tar.gz
helm package [chart name]
```

Get the remote index

```
wget https://raw.githubusercontent.com/anthonymag/helm-charts/refs/heads/main/index.yaml
```

Update the `index.html`

```
newchart=newchart-x.y.z
helm repo index --url https://github.com/anthonymag/helm-charts/releases/download/$newchart --merge index.yaml .
```

Confirm

```
cat index.html
```


