# This Dockerfile creates an debian image with avocado framework installed
#
# VERSION 0.1
FROM debian

MAINTAINER Dmitry Monakhov dmonakhov@openvz.org

# Install and clean in one step to decrease image size
ARG AVOCADO_PKG="fabric gdebi-core python-lzma python-pip python-pystache python-setuptools python-stevedore python-yaml"
RUN apt-get update && \
    apt-get -y install $AVOCADO_PKG && \
    pip install avocado-framework aexpect && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* \
       /usr/share/doc /usr/share/doc-base \
       /usr/share/man /usr/share/locale /usr/share/zoneinfo

CMD avocado
