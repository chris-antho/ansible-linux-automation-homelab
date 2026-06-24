# Ansible Linux Automation Homelab

This project uses Ansible to automate Ubuntu server configuration in my Proxmox homelab.

## Goals

 - Create Linux users
 - Install common packages
 - Configure SSH security settings
 - Install Docker
 - Deploy Node Exporter for Prometheus monitoring

## Lab Environment

 - Proxmox VE host
 - Ubuntu monitoring VM
 - Ubuntu target VM
 - Ansible control node
 - Prometheus and Grafana monitoring stack

## Ansible Connectivity Test

Verified Ansible connectivity to managed Ubuntu servers using:

```bash
ansible all -m ping
```

## Architecture

```text
Dell OptiPlex 7070 Micro
└── Proxmox VE
    ├── ubuntu-monitor
    │   ├── Ansible Control Node
    │   ├── Prometheus
    │   ├── Grafana
    │   ├── Alertmanager
    │   └── Node Exporter
    │
    └── ubuntu-target
        └── Node Exporter

Ansible Automation
├── User Creation
├── Package Installation
├── Docker Installation
└── Node Exporter Deployment
```

## Automated Tasks

This project automates the following configuration tasks across Ubuntu servers:

 - User creation and sudo configuration
 - Common package installation
 - Docker installation and service management
 - Node Exporter deployment for Prometheus monitoring

## Playbooks

```text
playbooks/
├── packages.yml
├── users.yml
├── docker.yml
├── node_exporter.yml
└── site.yml
```

## Running the Automation

Run all playbooks:

```bash
ansible-playbook playbooks/site.yml
```

Run individual playbooks:

```bash
ansible-playbook playbooks/packages.yml
ansible-playbook playbooks/users.yml
ansible-playbook playbooks/docker.yml
ansible-playbook playbooks/node_exporter.yml
```

## Skills Demonstrated

- Linux Administration
- Ansible Automation
- Infrastructure as Code (IaC)
- Docker
- Monitoring and Observability
- SSH Administration
- Git and GitHub
- Multi-Server Management
