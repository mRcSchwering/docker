# python base numpy

Base python with numpy and pandas.

```
docker login -u="mrcschwering"

MY_DOCKER_TAG="mrcschwering/python-base-numpy"
docker build -t "$MY_DOCKER_TAG:latest" .
docker push "$MY_DOCKER_TAG:latest"
```