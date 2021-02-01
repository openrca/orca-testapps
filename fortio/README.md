# Fortio

## Installation

Deploy chart release:

```
$ helm install --name fortio --namespace load-gen .
```

Port-forward:

```
$ kubectl -n load-gen port-forward svc/fortio 8082
```

## Uninstallation

Delete chart release:

```
$ helm delete --purge fortio
```
