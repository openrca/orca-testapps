# Fortio

## Installation

Deploy chart release:

```
$ helm install --name fortio --namespace load .
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
