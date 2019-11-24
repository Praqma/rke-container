# Rancher RKE Container

This repository contain a container version of [Rancher RKE](https://github.com/rancher/rke) - [LICENSE](https://github.com/rancher/rke/blob/master/LICENSE).

Typical usage with `cluster.yml` and e.g. ssh-key material in current working directory:

```shell
$ docker run --rm --user $(id -u):$(id -g) -v $(pwd):/work:rw  michaelvl/rke up
```

Note that when testing a Rancher RKE-based Kubernetes with Sonobuoy, the
unscheduable `controlplane` nodes must be labelled as `masters`. Rancher RKE
labels them as `controlplane`. Use the following command to label master nodes:

```shell
$ kubectl label node --selector node-role.kubernetes.io/controlplane="true" node-role.kubernetes.io/master="true"
```
