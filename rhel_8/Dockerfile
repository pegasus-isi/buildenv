FROM rockylinux:8

#%environment
#    PATH=/usr/lib64/mpich/bin:/usr/local/bin:/usr/bin:/bin

RUN dnf -y update 
RUN echo 'module_hotfixes=true' >>/etc/yum.repos.d/Rocky-PowerTools.repo
RUN dnf -y install epel-release

RUN dnf -y install --allowerasing --nobest --enablerepo=powertools \
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
        java-11-openjdk-devel \
        libffi-devel \
        libxml2-devel \
        libxslt-devel \
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
        rpm-sign \
        sqlite-devel \
        tar \
        wget \
        which \
        zlib-devel

# Python test requirements - FIXME: not a great idea to use pip3 install in this container
RUN pip3 install tox

# Documentation - FIXME: not a great idea to use pip3 install in this container
RUN pip3 install sphinx recommonmark sphinx_rtd_theme sphinxcontrib-openapi javasphinx mistune==0.8.4

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime


