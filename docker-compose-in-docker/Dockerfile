FROM docker/compose:debian-1.27.4

LABEL purpose="Image for gitlab worker with docker and docker-compose"
LABEL maintainer="schweringmarc01@gmail.com"

RUN apt-get update && apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

CMD ["docker-compose", "--version"]
