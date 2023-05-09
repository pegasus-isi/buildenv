FROM centos:7

#%environment
#    # needed for python test
#    export LANG=en_US.UTF-8

RUN yum -y install epel-release
RUN yum -y install ant | /bin/true
RUN yum -y install \
        ant-apache-regexp \
        ant-junit \
        bc \
        bzip2-devel \
        cryptsetup \
        curl-devel \
        epel-release \
        gcc \
        gcc-c++ \
        git \
        golang \
        java-1.8.0-openjdk-devel \
        libffi-devel \
        libseccomp-devel \
        libuuid-devel \
        make \
        mpich-devel \
        mysql-devel \
        openssl-devel \
        patch \
        postgresql-devel \
        python2-devel \
        python2-packaging \
        python2-virtualenv \
        python36-attr \
        python36-devel \
        python36-GitPython \
        python36-pip \
        python36-pyOpenSSL \
        python36-pytest \
        python36-PyYAML \
        python36-setuptools \
        python36-setuptools_scm \
        R-devel \
        readline-devel \
        rpm-build \
        singularity \
        sqlite-devel \
        squashfs-tools \
        tar \
        wget \
        which \
        yum-plugin-priorities \
        zlib-devel 

# Python test requirements - FIXME: not a great idea to use pip3 install in this container
RUN pip3 install tox==3.20.1

# Documentation - FIXME: not a great idea to use pip3 install in this container
RUN pip3 install sphinx recommonmark sphinx_rtd_theme sphinxcontrib-openapi javasphinx mistune==0.8.4

# Set Timezone
RUN cp /usr/share/zoneinfo/America/Los_Angeles /etc/localtime


