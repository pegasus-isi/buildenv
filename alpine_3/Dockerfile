FROM alpine:3.24

RUN apk add --update \
         apache-ant \
         bash \
         cargo \
         cmake \
         curl \
         g++ \
         gcc \
         git \
         libffi-dev \
         libxml2-dev \
         libxslt-dev \
         linux-headers \
         linux-pam \
         make \
         musl-dev \
         openjdk8 \
         openssl-dev \
         perl \
         py3-pip \
         py3-setuptools \
         py3-tox \
         py3-yaml \
         py3-gitpython \
         python3-dev \
         rust \
         sqlite-dev \
         wget \
         go

RUN pip3 install --break-system-packages build scikit-build-core
