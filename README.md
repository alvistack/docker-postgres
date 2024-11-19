# Docker Image Packaging for PostgreSQL

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![GitLab pipeline
status](https://img.shields.io/gitlab/pipeline/alvistack/docker-postgres/master)](https://gitlab.com/alvistack/docker-postgres/-/pipelines)
[![GitHub
tag](https://img.shields.io/github/tag/alvistack/docker-postgres.svg)](https://github.com/alvistack/docker-postgres/tags)
[![GitHub
license](https://img.shields.io/github/license/alvistack/docker-postgres.svg)](https://github.com/alvistack/docker-postgres/blob/master/LICENSE)
[![Docker
Pulls](https://img.shields.io/docker/pulls/alvistack/postgres-16.svg)](https://hub.docker.com/r/alvistack/postgres-16)

PostgreSQL is a powerful, open source object-relational database system.
It has more than 15 years of active development and a proven
architecture that has earned it a strong reputation for reliability,
data integrity, and correctness.

Learn more about PostgreSQL: <https://www.postgresql.org/>

## Supported Tags and Respective Packer Template Links

- [`alvistack/postgres-17`](https://hub.docker.com/r/alvistack/postgres-17)
  - [`packer/docker-17/packer.json`](https://github.com/alvistack/docker-postgres/blob/master/packer/docker-17/packer.json)
- [`alvistack/postgres-16`](https://hub.docker.com/r/alvistack/postgres-16)
  - [`packer/docker-16/packer.json`](https://github.com/alvistack/docker-postgres/blob/master/packer/docker-16/packer.json)
- [`alvistack/postgres-15`](https://hub.docker.com/r/alvistack/postgres-15)
  - [`packer/docker-15/packer.json`](https://github.com/alvistack/docker-postgres/blob/master/packer/docker-15/packer.json)

## Overview

This Docker container makes it easy to get an instance of PostgreSQL up
and running.

Based on [Official Ubuntu Docker
Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

- Packaging by Packer Docker builder and Ansible provisioner in single
  layer
- Handle `ENTRYPOINT` with
  [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

For the `VOLUME` directory that is used to store the repository data
(amongst other things) we recommend mounting a host directory as a [data
volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes),
or via a named volume if using a docker version \>= 1.9.

Start PostgreSQL:

    # Pull latest image
    docker pull alvistack/postgres-16

    # Run as detach
    docker run \
        -itd \
        --name postgres \
        --publish 5432:5432 \
        --volume /var/lib/postgresql/data:/var/lib/postgresql/data \
        alvistack/postgres-16

**Success**. PostgreSQL is now available on port 5432.

## Versioning

### `alvistack/postgres:latest`

The `latest` tag matches the most recent [GitHub
Release](https://github.com/alvistack/docker-postgres/tags) of this
repository. Thus using `alvistack/postgres:latest` or
`alvistack/postgres` will ensure you are running the most up to date
stable version of this image.

### `alvistack/postgres:<version>`

The version tags are rolling release rebuild by
[Travis](https://travis-ci.com/alvistack/docker-postgres) in weekly
basis. Thus using these tags will ensure you are running the latest
packages provided by the base image project.

## License

- Code released under [Apache License 2.0](LICENSE)
- Docs released under [CC BY
  4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

- Wong Hoi Sing Edison
  - <https://twitter.com/hswong3i>
  - <https://github.com/hswong3i>
