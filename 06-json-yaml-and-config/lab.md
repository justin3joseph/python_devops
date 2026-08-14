# Lab 06 — Configuration-Driven Server Checker

## Objective
Build a server checker whose thresholds are stored in YAML.

## Create `config.yaml`
```yaml
server:
  name: web01

monitoring:
  cpu_threshold: 80
  memory_threshold: 80
  disk_threshold: 90
```

## Tasks
1. Install PyYAML.
2. Load the YAML file.
3. Read the server name.
4. Read all thresholds.
5. Print the configuration.
6. Use the values in monitoring conditions.

## Challenge
Create a second environment configuration without changing the Python code.

## Questions
1. Why separate configuration from code?
2. Why should secrets not be stored in Git?
