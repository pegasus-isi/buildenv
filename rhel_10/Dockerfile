FROM almalinux:10-kitten

RUN dnf -y update
RUN dnf -y install epel-release

RUN dnf -y install --allowerasing --nobest \
        ant-apache-regexp \
        ant-junit \
        bc \
        bzip2-devel \
        curl-devel \
        gcc \
        gcc-c++ \
        git \
        glibc-langpack-en \
        java-21-openjdk-devel \
        latexmk \
        libffi-devel \
        make \
        mpich-devel \
        mariadb-devel \
        openssl-devel \
        patch \
        postgresql-devel \
        python3-attrs \
        python3-devel \
        python3-GitPython \
        python3-pyOpenSSL \
        python3-pyyaml \
        python3-setuptools \
        readline-devel \
        rpm-build \
        sqlite-devel \
        tar \
        texlive-* \
        wget \
        which \
        zlib-devel && \
    pip3 install tox

ENV PATH=/usr/lib64/mpich/bin:/usr/local/bin:/usr/bin:/bin

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

