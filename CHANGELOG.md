# Docker Image Packaging for PostgreSQL

## 11.0.x-0alvistack1 - TBC

### Major Changes

  - Revamp CMD as upstream image
  - Add some debug utils
  - Add checksum for curl

## 11.0.0-0alvistack1 - 2018-10-29

### Major Changes

  - Upgrade Docker base image to postgres:11
  - Update dumb-init to v.1.2.2
  - Add pglogical, pgpool2 support
  - Add peer-finder for Kubernetes support
  - Always start apps with `gosu postgres`

## 10.3.0-0alvistack1 - 2018-03-31

  - Running PostgreSQL with Docker
  - Official PostgreSQL docker image based
  - Handle ENTRYPOINT with dumb-init
  - Hack original docker-entrypoint.sh for initialization only
