# Fortio

## Installation

Deploy chart release:

```
$ helm install fortio . \
    --namespace load \
    --create-namespace \
    --set nodeSelector.role=exp-control
```

Port-forward:

```
$ kubectl -n load port-forward svc/fortio 8082
```

## Uninstallation

Delete chart release:

```
$ helm delete --purge fortio
```
