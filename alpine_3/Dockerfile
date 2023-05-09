# need an image with glibc
FROM frolvlad/alpine-glibc:alpine-3.14_glibc-2.33

RUN apk add --update \
         apache-ant \
         bash \
         cargo \
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
         py3-attrs \
         py3-pip \
         py3-setuptools \
         py3-tox \
         py3-yaml \
         python3-dev \
         R \
         R-dev \
         rust \
         sqlite-dev \
         wget
    
RUN python3 -m pip install GitPython

