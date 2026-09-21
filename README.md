# AAP Automation

A growing set of Ansible playbooks for our fleet. We start with httpd; more playbooks will be added over time.

## Contents

- `httpd` — install and configure the httpd web server

## Requirements

- Ansible 2.14+
- A RHEL/EL host reachable over SSH

## Quick start

```bash
ansible-galaxy collection install -r requirements.yml
ansible-playbook -i inventory/inventory.yml playbooks/httpd.yml
```

## Usage in Ansible Automation Platform

1. Point an AAP project at this repository.
2. Create an inventory source from `inventory/inventory.yml`.
3. Add a job template per playbook (play `playbooks/<name>.yml`) with an SSH credential for `cloud-user`.
4. Run it against the relevant host group.

## Inventory

Edit `inventory/inventory.yml` to point groups at your hosts.

## Variables

Role defaults live in `playbooks/roles/<role>/defaults/main.yml` and can be overridden per host or as extra vars.

## License

MIT
