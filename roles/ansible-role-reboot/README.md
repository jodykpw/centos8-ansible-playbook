Ansible Role: Reboot
=========

Ansible role for managing system reboots

This role provides a flexible and controlled way to manage system reboots on target hosts. It allows you to perform system reboots as part of your Ansible playbooks, ensuring that the hosts are restarted gracefully and in a controlled manner.

Requirements
------------

None.

Role Variables
--------------

The pre-reboot delay is a period of time introduced before initiating the system reboot. It allows for a pause or wait time before the actual reboot takes place. This delay is typically used to ensure that certain tasks or processes are completed before the reboot. For example, you may need to apply configuration changes, install software updates, or gracefully stop services. By introducing a pre-reboot delay, you can ensure that these tasks are finished before triggering the system reboot.
        
   pre_reboot_delay: 5

The post-reboot delay is a period of time introduced after the system has been rebooted. It provides a waiting period after the reboot to allow the system to fully restart, initialize services, and stabilize before proceeding with the subsequent tasks or configurations. This delay ensures that the system is in a stable and operational state before continuing with the playbook execution. It allows time for any necessary services or configurations to initialize after the reboot.

  post_reboot_delay: 30

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        pre_reboot_delay: 5
        post_reboot_delay: 30
      roles:
        - ansible-role-reboot

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
