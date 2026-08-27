FROM debian:bookworm

RUN apt-get -y update && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install \
        ant \
        ant-optional \
        bc \
        build-essential \
        cmake \
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
        tar \
        texlive-fonts-recommended \
        texlive-latex-base \
        wget && \
    LATEST_GO=$(curl -sSL "https://go.dev/VERSION?m=text" | head -n 1) && \
    ARCH=$(uname -m | sed 's/x86_64/amd64/;s/aarch64/arm64/') && \
    wget "https://dl.google.com/go/${LATEST_GO}.linux-${ARCH}.tar.gz" && \
    tar -C /usr/local -xzf "${LATEST_GO}.linux-${ARCH}.tar.gz" && \
    rm "${LATEST_GO}.linux-${ARCH}.tar.gz" && \
    apt-get -y clean

ENV PATH=/usr/local/go/bin:$PATH

# Documentation
RUN pip3 install --break-system-packages --upgrade pip setuptools==66.1.1 tox build scikit-build-core auditwheel patchelf ninja

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime
