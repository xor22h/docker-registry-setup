# Docker registry with auth

This repository provides a simple example on how to setup the docker-registry with TLS, granular user permissions & S3 Storage (optional)

## Deployment quickstart

1. Copy `.env.example` as `.env` and modify env variables as needed
2. Run `./bin/createKeys` to generate TLS cert for JWT encryption
3. Decide on scenario:
    1. if using simple file-system based storage: `docker compose up -d`
    2. if using real AWS S3, modify S3 credentials in `docker-compose.s3.yaml` and `docker compose -f docker-compose.yaml -f docker-compose.s3.yaml up -d`
    3. if using Minio - `docker compose -f docker-compose.yaml -f docker-compose.minio.yaml up -d`

## Usage


More details: [https://xor22h.dev/deploying-docker-registry-with-acl-tls-and-s3/](https://xor22h.dev/deploying-docker-registry-with-acl-tls-and-s3/)
