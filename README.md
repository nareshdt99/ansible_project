# Ansible Project: Configure CA Certificates and Deploy Application

## Overview

This Ansible project automates the following tasks:
1. Configure standard CA certificates on the target hosts.
2. Install custom CA certificates in each target’s trust store.
3. Deploy a Python Flask application into a virtual environment.

## Prerequisites

- Ansible installed on the control node.
- Python and virtualenv installed on the target hosts.
- Target hosts accessible via SSH.

## Project Structure
ansible_project/
├── .git/
├── README.md
├── playbooks/
│   ├── main.yml
│   ├── tasks/
│   │   ├── ca_certificates.yml
│   │   ├── custom_ca_certificates.yml
│   │   ├── deploy_application.yml
│   ├── vars/
│   │   └── main.yml
│   ├── templates/
│   │   └── example_app.service.j2
├── files/
│   ├── custom_certs/
│   │   ├── custom_ca1.crt
│   │   └── custom_ca2.crt
|   |   └── custom_ca3.crt
|   |
│   └── application/
│       └── Example-1.1.1-py3-none-any.whl
|       └── app.py
└── inventory/
    └── hosts.ini



