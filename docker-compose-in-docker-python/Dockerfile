FROM docker/compose:debian-1.27.4

LABEL purpose="Running python tests while starting docker containers"
LABEL maintainer="schweringmarc01@gmail.com"

# python build deps
RUN apt-get update && apt-get install -y \
    build-essential \
    zlib1g-dev \
    libncurses5-dev \
    libgdbm-dev \
    libnss3-dev \
    libssl-dev \
    libsqlite3-dev \
    libreadline-dev \
    libffi-dev \
    curl \
    libbz2-dev \
    && rm -rf /var/lib/apt/lists/*

# build python3.8
RUN curl -O https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tar.xz && \
    tar -xf Python-3.8.2.tar.xz && \
    cd Python-3.8.2 && \
    ./configure --enable-optimizations --enable-loadable-sqlite-extensions && \
    make -j 4 && \
    make altinstall

# try to enable python and pip
RUN update-alternatives --install /usr/bin/python python /usr/local/bin/python3.8 1 && \
    echo -e '#!/bin/bash\npython3.8 -m pip "$@"' > /usr/bin/pip && \
    chmod +x /usr/bin/pip

