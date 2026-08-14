# Lab 14 — Python + DevOps Tool Integration

## Objective
Use Python to generate a simple Ansible inventory from structured data.

## Input
Create `servers.yaml`:
```yaml
servers:
  - name: web01
    ip: 192.168.56.11
  - name: web02
    ip: 192.168.56.12
```

## Tasks
1. Read YAML with Python.
2. Validate that every server has `name` and `ip`.
3. Generate `inventory.ini`.
4. Display the generated inventory.

## Expected Output
```ini
[web]
web01 ansible_host=192.168.56.11
web02 ansible_host=192.168.56.12
```

## Challenge
Reject duplicate server names and invalid IP addresses using Python's `ipaddress` module.

## Extension
Generate a JSON report containing the inventory and validation status.
