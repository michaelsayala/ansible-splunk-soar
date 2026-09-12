# Ansible Splunk SOAR

Ansible playbook for automating the installation and configuration of Splunk SOAR.

This project is designed to simplify the deployment of a Splunk SOAR server by automating common operating system preparation, package installation, configuration, and Splunk SOAR setup tasks.

## Features

* Automated Splunk SOAR installation
* Linux operating system preparation
* Required package installation
* Splunk SOAR service user and group creation
* Installation directory preparation
* Installer package management
* Configuration through Ansible variables
* Repeatable and idempotent deployment

## Project Structure

```text
.
├── group_vars/
│   └── ...
├── roles/
│   └── ...
├── inventory.yml.example
├── site.yml
└── .gitignore
```

## Requirements

* Ansible
* Linux server supported by Splunk SOAR
* Splunk SOAR installation package
* SSH access to the target server
* Appropriate privileges for system configuration

## Usage

Clone the repository:

```bash
git clone https://github.com/michaelsayala/ansible-splunk-soar.git
cd ansible-splunk-soar
```

Create your inventory from the example:

```bash
cp inventory.yml.example inventory.yml
```

Review and update the inventory and variables for your environment.

Run the playbook:

```bash
ansible-playbook -i inventory.yml site.yml
```

## Configuration

Environment-specific settings are managed through Ansible inventory and variables.

Sensitive information such as passwords should not be stored directly in the repository. Use **Ansible Vault** or another secure secret-management solution.

Example:

```bash
ansible-vault encrypt group_vars/all/vault.yml
```

## Purpose

This repository is part of a hands-on Splunk engineering lab focused on infrastructure automation and repeatable deployment using Ansible.

It demonstrates how Ansible can be used to automate Splunk SOAR infrastructure preparation and installation.
