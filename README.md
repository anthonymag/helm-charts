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

Stage and commit changes in the chart

```
# Don't commit the charts directory
git add <chartname>/Chart* <chartname>/values.yaml index.yaml
git commit -m "Update xyz in chart"
```

Tag the release
```
git tag chartname-version.of.release main
```

Push with tags
```
git push --tags
```

Upload the packaged chart to the release in GitHub.

## To update charts from submodules

```
git submodule update --remote submodules/<submodule_name>
```
