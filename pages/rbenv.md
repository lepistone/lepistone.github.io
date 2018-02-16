---
title: rbenv & pyenv
---
`rbenv` is a tool for managing different ruby versions. `pyenv` is a python
fork. Usage is more or less the same for the two.

## install
- install `libreadline-dev`, `libsqlite3-dev`, `libbz2-dev`
- `pyenv install -l`
- `pyenv install 3.4.1`
- `pyenv rehash`

## select
- `pyenv versions`
- `pyenv {global, shell, local} 3.4.1`
