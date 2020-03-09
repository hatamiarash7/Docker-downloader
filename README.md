# Docker image downloader

It's a Python scripts for interacting with Docker Hub without needing the Docker client itself.

It interacts with the Docker registry [HTTPS API v2](https://docs.docker.com/registry/spec/api/).

## Download image

#### Pull a Docker image

`python pull.py hello-world`

#### Pull with specific tag

`python pull.py mysql/mysql-server:8.0`

#### Pull from another address

`python pull.py mcr.microsoft.com/mssql-tools`

## Load image

You can load images using `docker load` as follow :

`docker load -i <file-name>.tar`

## Limitations

- Only support v2 manifests. Some registries ( like [quay.io](https://quay.io) ) which only uses v1 manifests, may not work.
- Some big images may fail to unzip during the extract process
