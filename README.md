
# Ansible Palybook for CyberMeet Install

Basic ansible script to instal CyberTeach in docker based on an openstack base debian image.

### Requirments

You need to have:
* debian/ubuntu base image installed
* global IPv4 address
* dns A record for the ipv4 address
* setup ssh server with sudo

## Prepare for install, config

#### Configure vars (dns and ipv4 email turn, etc)

Edit hosts to set host or hosts
Edit group_vars/mm.yml
Rename according your hosts, and Edit host_vars/meet.yml

##### TURN

Deploy a TURN Server Befor you proceed with Ansible Playbook

#### Advanced options

For more advanced options see group_vars/all.yml

## Install

### Install ansible external roles

```bash
ansible-galaxy install -r requirements.yml
```

### Run setup playbook

```bash
ansible-playbook -i hosts -u debian playbook.yml
```
