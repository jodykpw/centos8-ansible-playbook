Ansible Role: EPEL
=========

EPEL (Extra Packages for Enterprise Linux) is a repository for CentOS and other compatible Linux distributions. It provides a collection of additional software packages that are not included in the default CentOS repositories.

The EPEL repository is maintained by the Fedora Project and is designed to provide a wide range of open-source software packages that are commonly used but not included in the base CentOS distribution. These packages are thoroughly tested and follow strict guidelines to ensure compatibility and stability with CentOS.

EPEL repository offers packages in various categories, including development tools, system utilities, libraries, networking tools, security applications, and more. It is particularly useful for CentOS users who require access to a larger set of software packages or need specific tools or libraries that are not available in the standard repositories.

Requirements
------------

This Ansible role has been developed and thoroughly tested with Ansible Core version 2.15.0.

This role was designed for:

- CentOS 8 Stream
- RHEL 8

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      become: true
      roles:
        - ansible-role-epel

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com