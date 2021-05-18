---
layout: post
title: "Nocloud"
---
Some time ago, as people do, I set up a couple Raspberry Pis as simple webservers at home. I wanted to set them up in a somewhat automated but very simple way.

The things I wanted were basic: nginx serving some files, TLS certificates, automatic updates, key-based SSH access. I wanted to configure those things as code instead of typing commands and taking notes.

Among the configuration managers I picked Ansible which is very simple and doesn't require anything other than SSH access and Python on the managed machine. A basic Ansible setup doesn't have an agent, which I liked. I also didn't bother using many high level Ansible modules from the community: I just wanted to install a couple packages, add lines to configuration files and things like that.

I was happy with the result, but a part was missing: I had to setup SSH access before I could run Ansible for the first time, because Ansible uses SSH. This can be done easily, but still it was a couple manual steps I noted on a README involving among other things the ssh-copy-id script.

Then I forgot about it for a year or so. Then yesterday I wanted to set up another Raspberry Pi, but this time instead of Raspberry Pi OS, I decided to use Ubuntu 21.04. Even though I could set it up headless, I decided to hook it up to a screen just to see what it looked like.

I did see something interesting, actually. At the first boot, I could see *cloud-init* being run. Strange, I thought, this is definitely not the cloud. In public clouds like Google Cloud or AWS, when you provision a VM you are basically cloning a disk image on your new VM. At the first boot the cloned image must be slightly differentiated from all the others: it needs some sort of ID, a unique SSH host key, and it needs to give you - the GCP or AWS customer - access to it.

Then it suddenly made sense. For my Raspberry Pis, I was not running an installation. Instead, I was cloning to a memory card a disk image downloaded from the internet. This is pretty much the same that happens on public clouds. The steps I hacked together last year with ssh-copy-id and a couple other things were addressing a problem that public clouds also have. And this is exactly why the Ubuntu image for Raspberry Pi uses *cloud-init*: it needs to generate SSH keys, authorize keys, configure the network, setting up users, before anything can be run on it. Even before Ansible run, because it needs networking and SSH, for example.

Public clouds use different methods to tell to a newborn VM how it should be configured. For GCP and AWS, the VM can access a *Metadata Server* to do just that. The cloud-init tool has provider for all those vendor-specific providers of information. Interestingly, it is using the *NoCloud* provider for my Raspberry Pi.

One of the methods to provide information to the NoCloud provider is to edit the user-config file on the memory card itself. In my case, a couple lines of YAML to tell it to create a *lepistone* user and authorize the SSH public key found on Github, and another line to set the hostname are all I needed to be able to run Ansible to configure the Pi. This replaces completely my manual steps from a year ago!

It totally makes sense, except for the word *NoCloud*.
