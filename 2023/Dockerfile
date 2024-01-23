FROM amazonlinux:2023
LABEL maintainer="Michael Buluma"
ENV container=docker

ENV pip_packages "ansible"

# Install systemd -- See https://hub.docker.com/_/centos/
RUN yum -y update; yum clean all

# Install requirements. # TODO https://github.com/robertdebock/docker-amazonlinux-systemd/blob/master/Dockerfile
RUN yum yum -y install deltarpm epel-release initscripts systemd \
 && yum -y update \
 && yum -y install \
      sudo \
      which \
      python-pip \
 && yum clean all
