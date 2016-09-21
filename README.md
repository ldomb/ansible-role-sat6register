# Register a host with Red Hat Satellite 6
# Ansible Role: sat6register

## Role sat6register

This roles allows the registration of hosts of any kind running Red Hat Enterprise Linux 5,6,7 to a Red Hat Satellite 6 server. The role gives you the option to register your host with or without puppet as a configuration management tool. It also gives you the option of updateing the host to the latest patch level during registration. If you chose puppet as a configuration management tool you can also add a host group which will apply your puppet classes within that hostgroup during the puppet run.  

## Requirements

>= ansible 2.1

You need to have a working Red Hat Satellite 6 server in place with an activation key allowing you to register with Satellite 6.
To be sucessfull you need to add the following yum repos to the activationkey:

rhel-7-server-rpms
rhel-7-server-satellite-tools-6.2-rpms

## Role Variables

Available variables are listed below, along with default values:

sat6_fqdn: https://sat6ldo.rdu.salab.redhat.com
admin_user: admin
admin_pass: {{ vault_admin_pass }} 
org: redhat
loc: nyc
hostgroup: rhel7base or "false" if none
activationkey: ak-Reg_To_Library_soe_no_puppet or "false" if none
updatehost: "true" or "false"

## Dependencies

none

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: sat6register, sat6_fqdn: https://sat6ldo.rdu.salab.redhat.com }

## License

GPLv2

## Author Information
This role was created in 2016 by Laurent Domb
