# Module 11 — Python + Docker

## Objectives
- Understand Docker automation from Python.
- Run Docker CLI commands from Python.
- Inspect containers.
- Learn the Docker SDK approach.

## CLI Automation
```python
import subprocess

result = subprocess.run(
    ["docker", "ps", "--format", "{{.Names}}"],
    capture_output=True,
    text=True,
    check=True
)

print(result.stdout)
```

## Docker SDK
Install:
```bash
python3 -m pip install docker
```

Example:
```python
import docker

client = docker.from_env()

for container in client.containers.list(all=True):
    print(container.name, container.status)
```

## DevOps Uses
- Container health checks
- Automated cleanup
- Deployment validation
- Inventory reports
- Container monitoring
