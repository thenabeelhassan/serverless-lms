# Ansible

This directory contains Ansible playbooks used to provision and configure EC2 instances for tasks like setting up Jenkins or managing supporting infrastructure components.

## Contents

- `playbooks/` – Individual Ansible playbooks (e.g., Jenkins setup)
- `inventory/` – Hosts and connection details
- `roles/` – Reusable Ansible roles (optional)

## Usage

```bash
ansible-playbook -i inventory/hosts playbooks/setup-jenkins.yml
```