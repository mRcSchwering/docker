FROM linuxbrew/linuxbrew:1.9.3

LABEL purpose="Linuxbrew image with AWS SAM"
LABEL maintainer="schweringmarc01@gmail.com"

RUN brew tap aws/tap && \
    brew install aws-sam-cli && \
    brew install aws-sam-cli

ENV PATH="/home/linuxbrew/.linuxbrew/opt/python@3.8/bin:$PATH"

RUN sudo ln -s /home/linuxbrew/.linuxbrew/opt/python@3.8/bin/python3 /usr/bin/python && \
    sudo ln -s /home/linuxbrew/.linuxbrew/opt/python@3.8/bin/pip3 /usr/bin/pip

CMD sam --version
