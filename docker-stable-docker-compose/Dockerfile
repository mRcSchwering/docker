FROM docker:stable

LABEL purpose="Image for gitlab worker with docker and docker-compose"
LABEL maintainer="schweringmarc01@gmail.com"

RUN apk add --no-cache py-pip curl && pip install docker-compose~=1.23.0

CMD ["docker-compose", "--version"]
