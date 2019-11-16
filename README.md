# Rancher RKE Container

This repository contain a container version of [Rancher RKE](https://github.com/rancher/rke).

Typical usage with `cluster.yml` and e.g. ssh-key material in current working directory:

```shell
$ docker run --rm --user $(id -u):$(id -g) -v $(pwd):/work:rw  michaelvl/rke up
```
