# kustomize

## Structure
```
├── base
│   ├── ingress.yaml
│   ├── kustomization.yaml
│   ├── namespace.yaml
│   ├── nginx-service.yaml
│   ├── persistent-volume.yaml
│   └── web-deployment.yaml
└── overlays
    ├── dev
    │   ├── deployment-patch.yaml
    │   └── kustomization.yaml
    └── prod
        ├── deployment-patch.yaml
        └── kustomization.yaml
```
## build
```sh
kustomize build overlays/dev/
```

## apply kubernetes
```sh
kustomize build overlays/dev/ | kubectl apply -f -
```