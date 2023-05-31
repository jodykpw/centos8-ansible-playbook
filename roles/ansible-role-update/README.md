Ansible Role: Update
=========

Ansible role for system updates

This role provides a streamlined and automated way to perform system updates on target hosts using Ansible. It ensures that the latest software packages, security patches, and system updates are applied to the target systems, helping to maintain their stability, security, and compatibility.

Requirements
------------

This Ansible role has been developed and thoroughly tested with Ansible Core version 2.15.0.

This role was designed for:

- CentOS 8 Stream
- RHEL 8

Role Variables
--------------

Boolean option whether enable the exclude function.

    exclude_enabled: false

Option to exclude certain packages or package groups from being updated during a system update process.

    yum_dnf_exclude: 'exclude=kernel*, docker*, kube*'

Specify the desired state of a system package during package management tasks. It allows you to control how packages are handled based on their current state.

Choices:

 - `latest` (default): This value ensures that the package(s) are updated to the latest available version. If the package is already installed, Ansible will check for updates and install the latest version if available.

 - `present` This value ensures that the package(s) are present on the system, but it does not enforce updates. If the package is already installed, Ansible will not perform any updates.

```
update_state: 'latest'
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        exclude_enabled: false
        yum_dnf_exclude: 'exclude=kernel*, docker*, kube*'
        update_state: 'latest'
      roles:
        - ansible-role-update

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com