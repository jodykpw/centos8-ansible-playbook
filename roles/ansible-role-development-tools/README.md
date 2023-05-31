Ansible Role: Development-Tools
=========

Development Tools is a package group in CentOS that includes various software development tools and libraries commonly used for building and compiling software. These tools are often required when working on development projects or building software from source code.

These tools include core development tools such as

* asciidoc
* autoconf
* automake
* binutils
* bison
* byacc
* ctags
* diffstat
* elfutils-libelf-devel
* flex
* gcc
* gcc-c++ 
* gdb
* glibc-devel
* intltool
* jna
* libtool
* ltrace
* make
* patchutils
* perl-Fedora-VSP
* perl-Sys-Syslog
* perl-generators
* pesign
* redhat-rpm-config
* rpm-build
* rpm-sign
* source-highlight
* strace
* systemtap
* valgrind
* valgrind-devel

Requirements
------------

This Ansible role has been developed and thoroughly tested with Ansible Core version 2.15.0.

This role was designed for:

- CentOS 8 Stream
- RHEL 8

Role Variables
--------------
While the Development Tools package group is useful for software development and building applications, it is generally not recommended to install it on a production server. The Development Tools package group includes a variety of compilers, debuggers, and build tools that are typically unnecessary for a production environment.

    install_development_tools: false



Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        install_development_tools: true
      roles:
        - ansible-role-development-tools

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
