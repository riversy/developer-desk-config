# Developer Desktop Configurator
There are Ansible playbooks which help to configure developers environment for Magento dev

## Run MySQL inside Docker

```
docker run -d -p 3306:3306 -v /var/lib/mysql:/var/lib/mysql --restart always -e MYSQL_PASS="admin" --name=mysql --net=host tutum/mysql
```
## Setup own environment

Copy `vars/local.sample.yml` to `vars/local.yml` and set your own user name and path to working folder.

## Run ansible script

Run Ansible script that will setup your local environment.

```
ansible-playbook lamp.yml -i inventory/prod --ask-sudo-pass
```

## Preinstall

Surely you need to have [Docker](https://docs.docker.com/engine/installation/) and [Ansible](http://docs.ansible.com/ansible/intro_installation.html) onboard.
