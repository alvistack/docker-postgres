# Docker Image Packaging for PostgreSQL

[![Travis](https://img.shields.io/travis/alvistack/docker-postgres.svg)](https://travis-ci.org/alvistack/docker-postgres)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-postgres.svg)](https://github.com/alvistack/docker-postgres/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-postgres.svg)](https://github.com/alvistack/docker-postgres/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/postgres.svg)](https://hub.docker.com/r/alvistack/postgres/)

PostgreSQL is a powerful, open source object-relational database system. It has more than 15 years of active development and a proven architecture that has earned it a strong reputation for reliability, data integrity, and correctness.

Learn more about PostgreSQL: <https://www.postgresql.org/>

## Supported Tags and Respective `Dockerfile` Links

  - [`latest` (master/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/master/Dockerfile)
  - [`11` (11/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/11/Dockerfile)
  - [`10` (10/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/10/Dockerfile)
  - [`9.6` (9.6/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/9.6/Dockerfile)
  - [`9.5` (9.5/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/9.5/Dockerfile)
  - [`9.4` (9.4/Dockerfile)](https://github.com/alvistack/docker-postgres/blob/9.4/Dockerfile)

## Overview

This Docker container makes it easy to get an instance of PostgreSQL up and running.

Based on [Official PostgreSQL Docker Image](https://hub.docker.com/_/postgres/) with some minor hack:

  - Handle `ENTRYPOINT` with [dumb-init](https://github.com/Yelp/dumb-init)

### Quick Start

For the `VOLUME` directory that is used to store the repository data (amongst other things) we recommend mounting a host directory as a [data volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes), or via a named volume if using a docker version \>= 1.9.

Start PostgreSQL:

    # Pull latest image
    docker pull alvistack/postgres
    
    # Run as detach
    docker run \
        -itd \
        --name postgres \
        --publish 5432:5432 \
        --volume /var/lib/postgresql/data:/var/lib/postgresql/data \
        alvistack/postgres

**Success**. PostgreSQL is now available on port 5432.

## Versioning

The `latest` tag matches the most recent version of this repository. Thus using `alvistack/postgres:latest` or `alvistack/postgres` will ensure you are running the most up to date version of this image.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
