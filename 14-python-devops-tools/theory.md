# Module 14 — Python + DevOps Tools

## Objectives
- Understand where Python fits around Ansible and Terraform.
- Use Python for glue automation.
- Generate inventories/configuration.
- Validate automation inputs.

## Python as Glue
Python is often used to connect tools:
```text
API → Python → JSON/YAML → Ansible/Terraform → Deployment
```

Python should not replace specialized tools unnecessarily. Use the right tool for the task.

## Ansible
Python can:
- Generate inventory data.
- Query APIs.
- Prepare variables.
- Validate configuration before a playbook runs.

## Terraform
Python can:
- Generate input data.
- Validate environment settings.
- Call external APIs.
- Produce reports after infrastructure operations.

## DevOps Principle
Keep infrastructure state and deployment logic in the appropriate tool. Use Python for automation glue, validation, reporting and integrations.
