# Isotope Tree

![App graph](./media/app-graph.png)

This test app was generated using [Istio Isotope](https://github.com/istio/tools/tree/master/isotope).

## Installation

Create namespace:

```
$ kubectl create ns isotope
```

Label namespace for Istio sidecar injection:

```
$ kubectl label ns isotope istio-injection=enabled
```

Deploy chart release:

```
$ helm install --name isotope-tree --namespace isotope . \
    --set replicaCount=1 \
    --set resources.requests.cpu=100m \
    --set resources.requests.memory=100Mi \
    --set resources.limits.cpu=1000m \
    --set resources.limits.memory=100Mi
```


## Uninstallation

Delete chart release:

```
$ helm delete --purge isotope-tree
```
