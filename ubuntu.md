---
title: ubuntu
layout: cheatsheet
---
## upgrade
- `apt-get update`
- `apt-get dist-upgrade  # more aggressive than upgrade, good the 1st time`
- `reboot`

## mark manual
- `apt-mark showmanual | xargs sudo apt-mark auto`
- `sudo apt-mark unmarkauto ubuntu-desktop ubuntu-standard ubuntu-minimal \`
  `ubuntu-restricted-addons linux-generic language-pack-gnome-en \`
  `intel-microcode gnome-themes-standard  # dmeventd`
- `apt-get autoremove [--simulate]`
- `apt-cache --installed rdepends firefox   # aptitude why firefox`
- Now you can `apt-mark showauto`

## apt-get install
- openssh-server
- vim-gnome  # even if used in a terminal, this gives you +clipboard
- git
- postgresql
- libpq-dev
- python-dev
- libxml2-dev 
- libxslt-dev
- libsasl2-dev
- libldap-dev
- libjpeg-dev

## python
Use the python executable provided by ubuntu, but use pip to manage python
packages. Every project will have its own virtualenv.
- sudo easy_install pip
- sudo pip install -U pip setuptools
- sudo pip install virtualenv

## postgres
- `sudo -u postgres createuser -s $USER`
- `createdb $USER`

## video
Compute the correct dpi, and
- `randr --dpi 9`
