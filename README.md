# metallb-kustomization

## Add the GitRepository

```bash
flux create source git metallb \
  --url=https://github.com/dashaun-cloud/metallb-kustomization \
  --branch=main \
  --export > ./clusters/arkansas/metallb-source.yaml
```

## Add the Kustomization

```bash
flux create kustomization metallb \
  --source=metallb \
  --path="./kustomize" \
  --prune=true \
  --export > ./clusters/arkansas/metallb-kustomization.yaml
```
