# docker:stable docker-compose python

When running pytests while starting docker containers and using `docker-compose`.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/docker-stable-docker-compose-python"
docker build -t "$MY_DOCKER_TAG:latest" .
docker push "$MY_DOCKER_TAG:latest"
```