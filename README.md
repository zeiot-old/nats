# RPI Nats

* Master : [![Circle CI](https://circleci.com/gh/zeiot/rpi-nats/tree/master.svg?style=svg)](https://circleci.com/gh/zeiot/rpi-nats/tree/master)
* Develop : [![Circle CI](https://circleci.com/gh/zeiot/rpi-nats/tree/develop.svg?style=svg)](https://circleci.com/gh/zeiot/rpi-nats/tree/develop)

Docker image of [Nats][] to use on a [Raspberry PI][].

Exposes Ports : `4222`, `8222` and `6222`

Configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker):

    $ docker run --rm --privileged multiarch/qemu-user-static:register --reset

Then you can run an armhf image from your x86_64 Docker host :

    $ make run version=0.9

Or build :

    $ make build version=0.9


# Usage

Launch Nats server:

    $ make run version=0.9

On another terminal :

    $ curl http://localhost:8222/varz


# Supported tags

* [![](https://images.microbadger.com/badges/version/zeiot/rpi-nats.svg)](http://microbadger.com/images/zeiot/rpi-nats "Get your own version badge on microbadger.com")


## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Raspberry PI]: https://www.raspberrypi.org/
[Nats]: https://nats.io/
