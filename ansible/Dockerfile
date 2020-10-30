# use the latest ubuntu image
FROM ubuntu:latest

# some lables - maybe add some more?
LABEL maintainer="12394156+jpylypiw@users.noreply.github.com"
LABEL version="0.0.1"
LABEL description="This is a custom docker image for ansible playbooks, roles and linting"

# do not prompt me for anything
ENV DEBIAN_FRONTEND=noninteractive

# update apt and install some packages
RUN apt-get update \
    && apt-get -y upgrade \
    && apt-get install -y python3-pip python3-dev sudo expect

# set alias python3 which is basically python
RUN ln -s /usr/bin/python3 /usr/local/bin/python

# install and update some pip packages
RUN pip3 install --upgrade pip ansible ansible-lint yamllint
