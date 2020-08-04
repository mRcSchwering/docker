# CPU-only Machine Learning Base

Base image for machine learning stuff.
Based on a very small (150MB) alpine-based Miniconda.
Adds CPU-only pytorch.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/ml-base-cpuonly"
TORCH_V="torch1.6"

docker build -t "$MY_DOCKER_TAG:latest" .
docker tag "$MY_DOCKER_TAG:latest" "$MY_DOCKER_TAG:$TORCH_V"
docker push "$MY_DOCKER_TAG:latest"
docker push "$MY_DOCKER_TAG:$TORCH_V"
```
