# docker:stable and docker-compose

Created for gitlab runners to use as docker-in-docker (`service: dind`).

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/docker-stable-docker-compose"
docker build -t "$MY_DOCKER_TAG:latest" .
docker push "$MY_DOCKER_TAG:latest"
```