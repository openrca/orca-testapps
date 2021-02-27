# Fortio

## Installation

Deploy chart release:

```
$ helm install fortio . \
    --namespace load \
    --create-namespace \
    --set resources.requests.cpu=1000m \
    --set resources.requests.memory=100Mi \
    --set resources.limits.cpu=4000m \
    --set resources.limits.memory=100Mi \
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
