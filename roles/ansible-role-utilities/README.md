Ansible Role: Utilities
=========

Ansible role for managing system utilities

The utilities role provides a collection of common system utilities and tools that can be useful for managing and configuring target hosts. It simplifies the installation and configuration of various utilities, enhancing the functionality and capabilities of the systems being managed.

Requirements
------------

None.

Role Variables
--------------

Boolean option used to install the system utilities on target hosts

- `wget`: is a command-line tool for downloading files from the web using various protocols.
- `curl`: is a command-line tool for making HTTP, HTTPS, and FTP requests, enabling you to interact with web services and download files.
- `net-tools`: is a package containing command-line networking tools for Linux, providing functionality for network configuration, monitoring, diagnostics, and information display. 
- `lsof`: is a command-line tool for listing open files and network sockets on a Linux system, providing insights into processes and their file or network connections.
- `bash-completion`: is a package that enhances the Bash shell by enabling intelligent tab-completion for commands, options, and file names, improving productivity and ease of use on the command line.
- `bind-utils`: is a package containing command-line utilities for managing and troubleshooting DNS on Linux systems, providing functionality for DNS queries, lookups, record checking, and diagnostics.
- `tree`: is a command-line tool that displays directory structures in a tree format, making it easy to visualize the organization of files and directories.
- `traceroute`: is a command-line tool used to trace the network path between a source and destination, revealing the intermediate routers or hops along the way, aiding in network troubleshooting and diagnosing connectivity problems.
- `psmisc`: is a package containing command-line utilities for managing and inspecting running processes on a Linux system, providing functionality for process monitoring, termination, and administrative tasks.
- `yum-utils`:  is a package containing command-line utilities and plugins that enhance the functionality of the YUM package manager, providing additional tools for package management, dependency resolution, repository management, and package analysis.

```
install_system_utilities: true
```

Command-line tool for creating, manipulating, and extracting archive files, providing compression options and preserving file metadata.

    install_tar: true


Command-line tool for creating, manipulating, and extracting compressed archive files in the ZIP format, providing options for compression, encryption, and splitting archives.
    
    install_zip: true

Feature-rich and highly configurable text editor known for its powerful editing capabilities, syntax highlighting, and extensibility, making it a popular choice among developers and system administrators.
    
    install_vim: true

Lightweight and user-friendly command-line text editor that offers basic editing features and a straightforward interface, making it suitable for quick edits and simple text manipulation tasks.
    
    install_nano: true

An interactive command-line process viewer and system monitoring tool that provides real-time information about system resources and processes, offering advanced features for managing and manipulating processes in a user-friendly interface.
    
    install_htop: true

A package containing command-line utilities and daemons for working with NFS, facilitating the configuration, management, and troubleshooting of NFS shares and clients in a Linux environment.
    install_nfs_utils: false

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        install_system_utilities: true
        install_tar: true
        install_zip: true
        install_vim: true
        install_nano: true
        install_htop: true
        install_nfs_utils: true
      roles:
        - ansible-role-utilities

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
