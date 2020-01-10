FROM mrcschwering/docker-stable-docker-compose

LABEL purpose="Running python tests while starting docker containers"
LABEL maintainer="schweringmarc01@gmail.com"

# add python3 pip
RUN apk add --no-cache python3 && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade pip setuptools && \
    if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    if [[ ! -e /usr/bin/python ]]; then ln -sf /usr/bin/python3 /usr/bin/python; fi && \
    rm -r /root/.cache

# useful libs for testing
RUN pip3 install docker requests pytest
