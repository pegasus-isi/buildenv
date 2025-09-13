FROM rockylinux:9

RUN dnf -y update
RUN dnf -y install epel-release

RUN dnf -y install --allowerasing --nobest --enablerepo=devel \
        ant-apache-regexp \
        ant-junit \
        bc \
        bzip2-devel \
        createrepo \
        curl-devel \
        gcc \
        gcc-c++ \
        git \
        glibc-langpack-en \
        gnupg2 \
        java-21-openjdk-devel \
        latexmk \
        libffi-devel \
        make \
        mpich-devel \
        mysql-devel \
        openssl-devel \
        patch \
        pinentry \
        postgresql-devel \
        python3-devel \
        python3-GitPython \
        python3-pyOpenSSL \
        python3-pytest \
        python3-pyyaml \
        python3-setuptools \
        python3-setuptools_scm \
        readline-devel \
        rpm-build \
        rpm-sign \
        sqlite-devel \
        tar \
        texlive-* \
        wget \
        which \
        zlib-devel && \
    pip3 install tox uv

ENV PATH=/usr/lib64/mpich/bin:/usr/local/bin:/usr/bin:/bin

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

