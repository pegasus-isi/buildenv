FROM rockylinux:9

RUN dnf -y update
RUN dnf -y install epel-release

RUN dnf -y install --allowerasing --nobest --enablerepo=devel \
        ant-apache-regexp \
        ant-junit \
        bc \
        bzip2-devel \
        curl-devel \
        gcc \
        gcc-c++ \
        git \
        glibc-langpack-en \
        java-11-openjdk-devel \
        libffi-devel \
        make \
        mpich-devel \
        mysql-devel \
        openssl-devel \
        patch \
        postgresql-devel \
        python3-attrs \
        python3-devel \
        python3-GitPython \
        python3-pyOpenSSL \
        python3-pytest \
        python3-pyyaml \
        python3-setuptools \
        python3-setuptools_scm \
        R-devel \
        readline-devel \
        rpm-build \
        sqlite-devel \
        tar \
        wget \
        which \
        zlib-devel && \
    pip3 install tox

ENV PATH=/usr/lib64/mpich/bin:/usr/local/bin:/usr/bin:/bin

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

