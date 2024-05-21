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


## Steps to Set Up the Project

### 1. Clone the Repository

## Steps to Set Up the Project

### 1. Clone the Repository
git clone <https://github.com/nareshdt99/ansible_project>
cd ansible_project

### 2. Configure Git
Set your global Git configuration:
git config --global user.name "naresh"
git config --global user.email "nareshdt99@example.com"

### 3. Define Inventory
Edit inventory/hosts.ini to specify your target hosts:
target_host ansible_host=your_target_host_ip ansible_user=your_user ansible_ssh_pass= your_passwd

### 4. Set Variables
Edit playbooks/vars/main.yml to set the variables:
app_port: 5000
app_deploy_location: /opt/example
app_wheel_file: Example-1.1.1-py3-none-any.whl

### 5. Run the Playbook
Execute the main playbook:
ansible-playbook -i inventory/hosts.ini playbooks/main.yml


