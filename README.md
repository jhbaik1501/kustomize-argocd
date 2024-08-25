# kustomize

## Structure
```
├── base
│   ├── configmap.yaml
│   ├── deployment-db.yaml
│   ├── deployment.yaml
│   ├── ingress.yaml
│   ├── kustomization.yaml
│   └── secret.yaml
└── overlays
    └── dev
        └── kustomization.yaml
```
## build
```sh
kustomize build overlay/dev/
```

## apply kubernetes
```sh
kustomize build overlay/dev/ | kubectl apply -f -
```