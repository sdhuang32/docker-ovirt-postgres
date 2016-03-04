# docker-ovirt-postgres
Slightly modified version of the official postgres image from dockerhub which works with ovirt-engine.

Currently the only addition is that it sets `max_connections` to 150 which is required by ovirt-engine.

Minimal usage:

```bash
docker run --name ovirt-postgres -e POSTGRES_PASSWORD=engine -e POSTGRES_USER=engine -e POSTGRES_DB=engine -d rmohr/ovirt-postgres
```

The numer of the allowed connections can be customized by setting the environment variable `MAX_CONNECTIONS` to the desired value:

```bash
docker [...] -e MAX_CONNECTIONS=200 -d rmohr/ovirt-postgres
```
