# docker-cli53
cli53 docker image based on library/python:2-onbuild

## Installation

Get the [trusted build on the docker hub](https://registry.hub.docker.com/u/ofertia/docker-cli53/):

```bash
$ docker pull ofertia/docker-cli53
```

or download and compile the source yourself from Github:

```bash
$ git clone https://github.com/ofertia/docker-cli53.git
$ cd docker-cli53
$ docker build -t ofertia/docker-cli53 .
```

## Usage

[cli53](https://github.com/barnybug/cli53) is a Command line script to administer the Amazon Route 53 dns service:

```bash
$ docker run --rm \
  -e AWS_ACCESS_KEY_ID="your aws access key" \
  -e AWS_SECRET_ACCESS_KEY="your aws secret key" \
  ofertia/docker-cli53 list
```

```bash
$ docker run --rm \
  -v ~/.boto:/home/user/.boto \
  ofertia/docker-cli53 list
```
