# AWS SAM

Linuxbrew image with [SAM framework](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) installed.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/awssam"
SAM_VERSION="sam1.15.0"

docker build -t "$MY_DOCKER_TAG:latest" .
docker tag "$MY_DOCKER_TAG:latest" "$MY_DOCKER_TAG:$SAM_VERSION"
docker push "$MY_DOCKER_TAG:latest"
docker push "$MY_DOCKER_TAG:$SAM_VERSION"
```
