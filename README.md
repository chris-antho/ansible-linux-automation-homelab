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
