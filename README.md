# Docker image downloader

There is 2 scripts for interacting with Docker Hub without needing the Docker client itself.

It interacts with the Docker registry [HTTPS API v2](https://docs.docker.com/registry/spec/api/).

---

## Python version

Examples :

```bash
python pull.py <image-name>:<tag>


python pull.py hello-world
python pull.py prom/prometheus:v2.19.2
python pull.py mcr.microsoft.com/mssql-tools
```

### Limitations

- Only support v2 manifests. Some registries ( like [quay.io](https://quay.io) ) which only uses v1 manifests, may not work.
- Some big images may fail to unzip during the extract process

---

## Bash version

This script has not above limits. But you **can't** run this on windows

```bash
./pull.sh <directory_name> <image-name>:<tag>


./pull.sh prometheus prom/prometheus:v2.19.2
./pull.sh mysql-5.7 mysql:5.7
```

---

## Load image

You can load images using `docker load` like this :

```bash
docker load -i <file-name>.tar
```
---

## Support

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request :D

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
