# :earth_africa: fedora32 [![Build Status](https://travis-ci.com/bentaljaard/fedora.svg?branch=fedora32)](https://travis-ci.org/github/bentaljaard/fedora)

![](https://raw.githubusercontent.com/multiarch/dockerfile/master/logo.jpg)

Multiarch Fedora images for Docker.

* `multiarch/fedora` on [Docker Hub](https://hub.docker.com/r/multiarch/fedora/)
* [Available tags](https://hub.docker.com/r/multiarch/fedora/tags/)

## Usage

Once you need to configure binfmt-support on your Docker host.
This works locally or remotely (i.e using boot2docker or swarm).

```console
# configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker)
$ docker run --rm --privileged multiarch/qemu-user-static:register --reset
```

Then you can run an `aarch64` image from your `x86_64` Docker host `aarch64`

```console
$ docker run -it --rm bentaljaard/fedora:32-aarch64

root@34f68c7ec9ae:/# uname -a
Linux 34f68c7ec9ae 4.4.27-moby #1 SMP Wed Oct 26 14:21:29 UTC 2016 aarch64 aarch64 aarch64 GNU/Linux
root@34f68c7ec9ae:/#
```

## License

MIT
