FROM ghcr.io/computestacks/cs-docker-base:ubuntu-focal

LABEL maintainer="ComputeStacks <hello@computestacks.com>"
LABEL org.opencontainers.image.authors="https://computestacks.com"
LABEL org.opencontainers.image.source="https://github.com/ComputeStacks/cs-docker-maria-backup/tree/main/10.5"
LABEL org.opencontainers.image.url="https://github.com/ComputeStacks/cs-docker-maria-backup/tree/main/10.5"
LABEL org.opencontainers.image.title="Maria Backup 10.5"

RUN set -ex; \
    \
    apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8; \
    add-apt-repository 'deb [arch=amd64,arm64,ppc64el] http://sfo1.mirrors.digitalocean.com/mariadb/repo/10.5/ubuntu bionic main';

RUN set -ex; \
    \
    apt-get update; \
    apt-get install -y \
            mariadb-backup \
            mariadb-client \
    ; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*;
