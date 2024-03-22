FROM amazonlinux:1

LABEL maintainer="Michael Buluma <me@buluma.co.ke>"
LABEL build_date="2024-03-22"

ENV container=docker

RUN yum -y install upstart

VOLUME ["/sys/fs/cgroup"]
CMD ["/sbin/init"]
