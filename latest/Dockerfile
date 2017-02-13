FROM postgres:latest

ENV MAX_CONNECTIONS 150

RUN mkdir -p /docker-entrypoint-initdb.d

COPY ovirt-db-config.sh /docker-entrypoint-initdb.d/
