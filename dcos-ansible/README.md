# dcos-ansible

Inspired from https://github.com/OldCrowEW/dcos-ansible

This repo uses [Ansible](https://www.ansible.com/) to configure a [Mesosphere](https://mesosphere.com/) stack following the [DC/OS Advanced Installation Guide](https://dcos.io/docs/1.10/installing/custom/advanced/)

Currently all inventory IPs are hardcoded in the hosts.ini file. For now you must modify the following files with the correct values:

- [hosts.ini](https://github.com/backtonet/ansible_playbooks/blob/master/dcos-ansible/hosts.ini)
- [group_vars/all](https://github.com/backtonet/ansible_playbooks/blob/master/dcos-ansible/group_vars/all)

** Notice the hosts.ini file has hostname set with ansible_host= override to public IP.

## Usage
```
ansible-playbook -i hosts.ini playbook-dcos.yml -u centos --private-key=key.pem
```
