# `docker-images`

## How to build, tag, and push manually an example

```bash
cd /path/to/docker-images
export DIRNAME=debian-python3.10.0
```

Select Docker container registry:

**GitHub:**

see also: [GitHub: Working with the Container registry
](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)

```bash
export CR_PAT=<CONTAINER_REGISTRY_PERSONAL_ACCESS_TOKEN>  # see eWallet
echo $CR_PAT | docker login ghcr.io -u jamilraichouni --password-stdin
export DOCKER_REGISTRY=ghcr.io/jamilraichouni
```

**GitLab:**

```bash
export DOCKER_REGISTRY=registry.gitlab.com/jar1/docker-images
```

```bash
docker build --build-arg DOCKER_REGISTRY=$DOCKER_REGISTRY -t $DOCKER_REGISTRY/$DIRNAME:latest $DIRNAME;
docker push $DOCKER_REGISTRY/$DIRNAME:latest
```
