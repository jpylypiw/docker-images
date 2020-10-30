# Docker file for a slim Ubuntu-based Python3 image to run ansible and linting

FROM ubuntu:latest

LABEL maintainer="12394156+jpylypiw@users.noreply.github.com"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y python3-pip python3-dev \
    && cd /usr/local/bin \
    && ln -s /usr/bin/python3 python \
    && pip3 install --upgrade pip \
    && pip3 install --upgrade ansible \
    && pip3 install --upgrade ansible-lint \
    && pip3 install --upgrade yamllint
