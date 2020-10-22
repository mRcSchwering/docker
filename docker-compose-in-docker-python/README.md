# docker:stable docker-compose python

When running pytests while starting docker containers and using `docker-compose`.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/docker-stable-docker-compose-python"
PY_VERSION="python3.8"

docker build -t "$MY_DOCKER_TAG:latest" .
docker tag "$MY_DOCKER_TAG:latest" "$MY_DOCKER_TAG:$PY_VERSION"
docker push "$MY_DOCKER_TAG:latest"
docker push "$MY_DOCKER_TAG:$PY_VERSION"
```
