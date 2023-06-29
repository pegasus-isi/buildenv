FROM debian:bookworm

RUN apt-get -y update && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install \
        ant \
        ant-optional \
        bc \
        build-essential \
        curl \
        debhelper \
        default-jdk \
        g++ \
        gcc \
        git \
        libcurl4-openssl-dev \
        libffi-dev \
        libpq-dev \
        libsqlite3-dev \
        libssl-dev \
        lintian \
        locales-all \
        make \
        procps \
        python3-attr \
        python3-dev \
        python3-git \
        python3-openssl \
        python3-pika \
        python3-pip \
        python3-pytest \
        python3-setuptools \
        python3-setuptools-scm \
        python3-sphinx \
        python3-yaml \
        r-base \
        tar \
        texlive-fonts-recommended \
        texlive-latex-base \
        wget \
    && \
    apt-get -y clean

# Documentation
RUN pip3 install --break-system-packages --upgrade pip setuptools==45.3.0 tox

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

