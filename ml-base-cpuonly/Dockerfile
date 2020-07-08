# alpine miniconda
FROM frolvlad/alpine-miniconda3

LABEL purpose="miniconda+pip with cpuonly pytorch"
LABEL maintainer="schweringmarc01@gmail.com"

RUN conda install -y pip && \
    conda install -y pytorch torchvision cpuonly -c pytorch
