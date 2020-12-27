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

choice 1 (quickstart templ)
choice 1 (zip)
choice 2 (py38)
proj name sam-app
choice 1 (hello world)
rm -rf sam-app

sam init \
 --name test \
 --package-type Zip \
 --runtime python3.8 \
 --dependency-manager pip \
 --app-template hello-world
