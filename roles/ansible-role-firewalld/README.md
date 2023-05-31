Ansible Role: Firewalld
=========

An Ansible role that allows for the installation or disabling of the Firewalld firewall management tool on CentOS-based systems. This role provides the flexibility to enable or disable the Firewalld service based on your specific requirements.

Requirements
------------

This Ansible role has been developed and thoroughly tested with Ansible Core version 2.15.0.

This role was designed for:

- CentOS 8 Stream
- RHEL 8

Role Variables
--------------
By default, Firewalld is enabled and active on CentOS-based systems. However, in certain scenarios, you may want to leave Firewalld enabled and running. 

    enable_firewalld: true

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        enable_firewalld: true
      roles:
        - ansible-role-firewalld

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
