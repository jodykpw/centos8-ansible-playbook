# 📕 CENTOS 8 Cloud-Init DevBox Playbook

An Ansible playbook designed to set up a development environment on CentOS 8 using cloud-init. This playbook aims to automate the provisioning of a CentOS 8 virtual machine or cloud instance, specifically tailored for development purposes. It includes tasks to install common development tools and perform other necessary configurations to create a functional and ready-to-use development environment.

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
ansible-playbook init-localhost-server.yml -i dev.ini
```

## 📚 Available playbooks

- 📖 `localhost.yml` For auto configure a fresh localhost virtual server, one limitation of this playbook is that it requires a manual reboot after execution.

- 📖 `site.yml` For auto configure a fresh remote virtual server.

- 📖 `migrate-home-directory.yml` For move the home directory to a new partition on CentOS 8, for the requirements and dependencies please refer to ansible-role-migrate-home-dir README.md 

- 📖 `docker.yml` Integrated with the [geerlingguy/ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker).

## 📑 To Do

- [] `rsnapshot`: Contains tasks for configuring Rsnapshot backups.

Or more...

## 📄 License

MIT / BSD

## 🇬🇧🇭🇰 Author Information

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
