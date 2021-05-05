# Kustomize Configmap Generation Merge Example

This repo is an example of how to use the [configMapGenerator](https://kubectl.docs.kubernetes.io/references/kustomize/kustomization/configmapgenerator/#configmap-from-literals)
to merge custom configs from a more generic location (e.g. `overlay/`)
The reason why the configmap is being overridden in a `kustomization.yaml` file outside
the `postgres` directory is so it can be referenced by another resource.

## Usage

```
kubectl apply -k postgres/overlay
```
