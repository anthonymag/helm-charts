# helm-charts
Helm charts consumed by ArgoCD

To add a new chart

1. Add the chart normally, include the Chart.yaml, Chart.lock, values and templates. Do not include the charts directory
2. Add the new repo to the CI list in .github/workflows/release.yml

