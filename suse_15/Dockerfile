FROM opensuse/leap:15

RUN zypper update -y

RUN zypper install -y \
        ant-apache-regexp \
        ant-junit \
        bc \
        bzip2 \
        gcc \
        gcc-c++ \
        git \
        java-17-openjdk \
        libffi-devel \
        libmysqlcppconn-devel \
        libopenssl-devel \
        libxml2-devel \
        libxslt-devel \
        make \
        mpich-devel \
        patch \
        postgresql-devel \
        python3-devel \
        python3-pip \
        python3-pyaml \
        python3-pyOpenSSL \
        python3-pytest \
        python3-tox \
        python3-setuptools \
        python3-setuptools_scm \
        python311-devel \
        python311-pip \
        python311-setuptools \
        readline-devel \
        rpm-build \
        sqlite3-devel \
        tar \
        wget \
        which \
        zlib-devel && \
    python3 -m pip install tox

ENV PATH=/usr/lib64/mpi/gcc/mpich/bin:/usr/local/bin:/usr/bin:/bin

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime


