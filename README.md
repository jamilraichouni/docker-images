# `docker-images`

To manually build:

```bash
DIRNAME=debian-python3.10.0
docker build --build-arg DOCKER_REGISTRY=registry.gitlab.com/jar1/docker-images -t registry.gitlab.com/jar1/docker-images/$DIRNAME:latest $DIRNAME
```
