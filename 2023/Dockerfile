FROM amazonlinux:2023
LABEL maintainer="Michael Buluma"
ENV container=docker

ENV pip_packages "ansible"

# Install systemd -- See https://hub.docker.com/_/centos/
RUN yum -y update; yum clean all
