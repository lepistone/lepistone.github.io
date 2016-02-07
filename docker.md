---
title: docker
layout: cheatsheet
---
## docker machine
- `alias doma=docker-machine`
- `doma ls`
- `doma create default`
- `doma start`
- `eval $(doma env)`

## docker
- `docker exec` execute command in running container
- `docker images` list images
  - `docker rmi $(docker images -q)` remove all images
- `docker ps` list containers
  - `-a` include stopped)
  - `docker rm $(docker ps -aq)` remove all containers
- `docker run IMAGE COMMAND` run once in a new container (`-d` daemon)
  - `-it` interactive
  - `-d` daemon
- `docker top` show processes in container
