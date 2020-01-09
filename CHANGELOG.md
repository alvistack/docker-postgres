# Docker Image Packaging for PostgreSQL

## 11.5.0-XalvistackY - TBC

### Major Changes

  - Prepare postgresql.conf.sample as upstream image

## 11.5.0-2alvistack3 - 2019-11-05

### Major Changes

  - Upgrade minimal Ansible support to 2.9.0
  - Upgrade Travis CI test as Ubuntu Bionic based
  - Default with Python 3
  - Hotfix for en\_US.utf8 locale

## 11.5.0-1alvistack1 - 2019-10-18

### Major Changes

  - Revamp as Ansible based

## 11.3.0-0alvistack1 - 2019-05-20

### Major Changes

  - Bugfix "Build times out because no output was received"

## 11.2.0-0alvistack7 - 2019-04-16

### Major Changes

  - Remove legacy 9.3 support as upstream image
  - Improve checksum handling

## 11.2.0-0alvistack5 - 2019-03-18

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
