# Docker file for a slim Ubuntu-based Python3 image to run ansible and linting

FROM ubuntu:latest

LABEL maintainer="12394156+jpylypiw@users.noreply.github.com"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get -y upgrade \
    && apt-get install -y python3-pip python3-dev sudo \
    && ln -s /usr/bin/python3 /usr/local/bin/python \
    && pip3 install --upgrade pip ansible ansible-lint yamllint
