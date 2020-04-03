---
title: docker
---
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
