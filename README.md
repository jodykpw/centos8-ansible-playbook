# 📕 CENTOS 8 Ansible Playbook

An Ansible playbook designed to set up a development environment on CentOS 8. This playbook aims to automate the provisioning of a CentOS 8 virtual machine or cloud instance, specifically tailored for development purposes. It includes tasks to install common development tools and perform other necessary configurations to create a functional and ready-to-use development environment.

## 🗂️ The files structure is organised this way:
Based on [Ansible Best Practices: Sample directory layout](https://docs.ansible.com/ansible/latest/tips_tricks/sample_setup.html#sample-directory-layout)

## 🚀 Quick start

1. `git clone --recursive` this repository.
2. Go to the cloned folder.
3. Editing the group_vars files, you can customize variables specific to different groups of hosts in your Ansible inventory. These variables will be applied when running playbooks or tasks that target the corresponding group of hosts.
4. Select a playbook (see [`Available playbooks`](https://github.com/truewebartisans/useful-playbooks#-available-playbooks) section).
5. Run `<playbook_name>` -i `<inventory_name>`

Example

```console
ansible-playbook init-localhost-server.yml -i hosts.ini
```

## 📚 Available playbooks

- 📖 `init-localhost-server.yml` Is an Ansible playbook tailored for deploying configurations and initializing services on the local machine itself. 

- 📖 `init-remote-server.yml` Is an Ansible playbook designed for remote server initialization and configuration. 

- 📖 `docker.yml` Integrated with the [geerlingguy/ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker).

- 📖 `rsnapshot.yml` Is used to configure and manage the rsnapshot backup.

## 📑 To Do

- [] `podman`: Ansible Role for Podman Installation.

Or more...

## 📄 License

MIT / BSD

## 🇬🇧🇭🇰 Author Information

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
