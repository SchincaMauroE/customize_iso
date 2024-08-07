Role Name
=========

This a role created for modifying an ESXi iso to use a custom kickstart file for unattended deploy.

Requirements
------------

* Ansible
* ESXi iso file
* community.general

Role Variables
--------------

### defaults/main.yml

* esxi_root_passw: Password that should be set to the root user in the esxi host.
* esxi_ip: IP for the esxi host to use.
* esxi_hostname: Hostname for the esxi host to use.
* esxi_gateway: Gateway for the esxi host to use.
* esxi_netmask: Netmask for the esxi host to use.
* esxi_dns: DSN ip for the esxi host to use. Can be up to two ips.
* esxi_vlan: VLAN id for the esxi host to use.
* iso_file: ESXi iso file to use as base to modify.
* domains: Domains to add to the ESXi network config.

### vars/main.yml

* cdrom_mount_dir: Directory path to mount the iso file.
* cdrom_dir: Directory path copy the content of the iso file.

Dependencies
------------

Example Playbook
----------------

    - hosts: localhost
      roles:
         - role: customize_iso

License
-------

BSD

Author Information
------------------

* Oviedo Matias
* Schincha Mauro
