FROM amazonlinux:2023
LABEL maintainer="Michael Buluma"
LABEL build_date="2024-03-22"
ENV container=docker

ENV pip_packages "ansible"

# Install systemd -- See https://hub.docker.com/_/centos/
RUN dnf -y update; dnf clean all

# Install requirements. # TODO https://github.com/robertdebock/docker-amazonlinux-systemd/blob/master/Dockerfile
# RUN dnf -y install deltarpm epel-release initscripts systemd \
RUN dnf -y install initscripts systemd \
 && dnf -y update \
 && dnf -y install \
      sudo \
      which \
      python-pip

RUN dnf clean all

# Install Ansible via Pip.
RUN pip install $pip_packages

# Disable requiretty.
RUN sed -i -e 's/^\(Defaults\s*requiretty\)/#--- \1/'  /etc/sudoers

# Install Ansible inventory file.
RUN mkdir -p /etc/ansible
RUN echo -e '[local]\nlocalhost ansible_connection=local' > /etc/ansible/hosts

VOLUME ["/sys/fs/cgroup"]
CMD ["/usr/lib/systemd/systemd"]
