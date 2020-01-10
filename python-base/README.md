# python base

Alpine python with some basic libraries.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/python-base"
docker build -t "$MY_DOCKER_TAG:latest" .
docker push "$MY_DOCKER_TAG:latest"
```