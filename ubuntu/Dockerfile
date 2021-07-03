FROM ubuntu:20.04

ENV PATH="/root/miniconda3/bin:${PATH}"

RUN (yes | unminimize) \
    && apt install -y \
        build-essential vim git curl wget binutils-common

RUN DEBIAN_FRONTEND=noninteractive \
    apt install -y software-properties-common

RUN add-apt-repository ppa:deadsnakes/ppa \
    && apt update && apt install -y python3.9

ADD https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh \
    /tmp/Miniconda3-latest-Linux-x86_64.sh

RUN mkdir /root/.conda \
    && bash /tmp/Miniconda3-latest-Linux-x86_64.sh -b

WORKDIR /code



