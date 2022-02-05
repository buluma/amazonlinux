Docker Amazon Linux Systemd
===========================

This Dockerfile can build containers capable to use systemd.

[![Build 2018.03-1](https://github.com/buluma/amazonlinux/actions/workflows/build-1.yml/badge.svg)](https://github.com/buluma/amazonlinux/actions/workflows/build-1.yml) [![Build latest-2](https://github.com/buluma/amazonlinux/actions/workflows/build-2.yml/badge.svg)](https://github.com/buluma/amazonlinux/actions/workflows/build-2.yml)

Branches
--------

This repository has multiple branches that relate to amazonlinux versions.

|Branch |amazonlinux Version|Docker image tag|
|-------|-------------------|----------------|
|master |2                  |latest          |
|1      |1                  |1               |

Pull strategy
-------------

The different branches are **not** merged, they live as individual branches.

Manually starting
-----------------

```
docker run \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  buluma/amazonlinux
```
