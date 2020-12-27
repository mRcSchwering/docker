FROM linuxbrew/linuxbrew:1.9.3

LABEL purpose="Linuxbrew image with AWS SAM"
LABEL maintainer="schweringmarc01@gmail.com"

RUN brew tap aws/tap && \
    brew install aws-sam-cli && \
    brew install aws-sam-cli

CMD sam --version
