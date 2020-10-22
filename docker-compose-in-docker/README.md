# docker:stable and docker-compose

Created for gitlab runners to use as docker-in-docker (`service: dind`).

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/docker-compose-in-docker"
DC_VERSION="compose1.27"

docker build -t "$MY_DOCKER_TAG:latest" .
docker tag "$MY_DOCKER_TAG:latest" "$MY_DOCKER_TAG:$DC_VERSION"
docker push "$MY_DOCKER_TAG:latest"
docker push "$MY_DOCKER_TAG:$DC_VERSION"
```
