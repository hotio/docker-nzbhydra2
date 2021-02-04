[<img src="https://hotio.dev/img/nzbhydra2.png" alt="logo" height="130" width="130">](https://github.com/theotherp/nzbhydra2)

[![GitHub Source](https://img.shields.io/badge/github-source-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/hotio/nzbhydra2)
[![GitHub Registry](https://img.shields.io/badge/github-registry-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/orgs/hotio/packages/container/package/nzbhydra2)
[![Docker Pulls](https://img.shields.io/docker/pulls/hotio/nzbhydra2?color=ffb64c&style=flat-square&label=pulls&logo=docker&logoColor=white&labelColor=757575)](https://hub.docker.com/r/hotio/nzbhydra2)
[![Discord](https://img.shields.io/discord/610068305893523457?style=flat-square&color=ffb64c&label=discord&logo=discord&logoColor=white&labelColor=757575)](https://hotio.dev/discord)
[![Upstream](https://img.shields.io/badge/upstream-project-ffb64c?style=flat-square&labelColor=757575)](https://github.com/theotherp/nzbhydra2)
[![Website](https://img.shields.io/badge/website-hotio.dev-ffb64c?style=flat-square&labelColor=757575)](https://hotio.dev/containers/nzbhydra2)

## Starting the container

CLI:

```shell
docker run --rm \
    --name nzbhydra2 \
    -p 5076:5076 \
    -e PUID=1000 \
    -e PGID=1000 \
    -e UMASK=002 \
    -e TZ="Etc/UTC" \
    -e ARGS="" \
    -v /<host_folder_config>:/config \
    hotio/nzbhydra2
```

Compose:

```yaml
version: "3.7"

services:
  nzbhydra2:
    container_name: nzbhydra2
    image: hotio/nzbhydra2
    ports:
      - "5076:5076"
    environment:
      - PUID=1000
      - PGID=1000
      - UMASK=002
      - TZ=Etc/UTC
      - ARGS
    volumes:
      - /<host_folder_config>:/config
```

## Tags

| Tag                | Upstream            | Version | Build |
| -------------------|---------------------|---------|-------|
| `release` (latest) | GitHub releases     | ![version](https://img.shields.io/badge/dynamic/json?color=f5f5f5&style=flat-square&label=&query=%24.version&url=https%3A%2F%2Fraw.githubusercontent.com%2Fhotio%2Fnzbhydra2%2Frelease%2FVERSION.json) | ![build](https://img.shields.io/github/workflow/status/hotio/nzbhydra2/build/release?style=flat-square&label=) |
| `testing`          | GitHub pre-releases | ![version](https://img.shields.io/badge/dynamic/json?color=f5f5f5&style=flat-square&label=&query=%24.version&url=https%3A%2F%2Fraw.githubusercontent.com%2Fhotio%2Fnzbhydra2%2Ftesting%2FVERSION.json) | ![build](https://img.shields.io/github/workflow/status/hotio/nzbhydra2/build/testing?style=flat-square&label=) |

You can also find tags that reference a commit or version number.
