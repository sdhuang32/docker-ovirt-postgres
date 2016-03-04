FROM postgres:9.2.15

ENV MAX_CONNECTIONS 150

RUN mkdir -p /docker-entrypoint-initdb.d

COPY ovirt-db-config.sh /docker-entrypoint-initdb.d/
