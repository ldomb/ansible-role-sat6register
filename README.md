# README.md
# Ansible Role: Acme 2.x

NOT READY FOR USE YET

## Role sat6register

This roles allows the registration of hosts of any kind running Red Hat Enterprise Linux to a Red Hat Satellite 6 server. The role gives you the option to register your host with or without puppet as a configuration management tool. If you chose puppet as a configuration management tool you can also add a host group which will apply your puppet classes within that hostgroup during the puppet runs.  

## Requirements

>= ansible 2.1

You need to have a working satellite 6 server in place with an activation key allowing you to connect to satellite6. You need the following repos enabled:

rhel-7-server-rpms
rhel-7-server-satellite-tools-6.2-rpms

## Role Variables

Available variables are listed below, along with default values:

sat6_fqdn: https://sat6ldo.rdu.salab.redhat.com
admin_user: admin
admin_pass: valutpass
org: redhat
loc: nyc
hostgroup: rhel7base
activationkey: ak-Reg_To_Library_soe_no_puppet

## Dependencies

none

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: ldomb.sat6register }

## License

GPLv2

## Author Information
This role was created in 2016 by Laurent Domb
