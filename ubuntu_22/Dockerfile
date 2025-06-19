FROM ubuntu:22.04

RUN apt-get -y update && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install \
        ant \
        ant-optional \
        apt-utils \
        bc \
        build-essential \
        createrepo-c \
        curl \
        debhelper \
        default-jdk \
        dpkg-dev \
        g++ \
        gcc \
        git \
        libcurl4-openssl-dev \
        libffi-dev \
        libmysqlclient-dev \
        libpq-dev \
        libsqlite3-dev \
        libssl-dev \
        lintian \
        locales-all \
        mpich \
        pinentry-tty \
        python3-dev \
        python3-git \
        python3-openssl \
        python3-pika \
        python3-pip \
        python3-pytest \
        python3-setuptools \
        python3-setuptools-scm \
        python3-sphinx \
        python3-venv \
        python3-yaml \
        r-base \
        tar \
        wget

# Documentation
RUN pip3 install --upgrade pip setuptools==45.3.0 tox

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

