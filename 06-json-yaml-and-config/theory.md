# Module 06 — JSON, YAML and Configuration

## Objectives
- Read and write JSON.
- Read YAML configuration.
- Separate configuration from code.
- Understand nested configuration data.

## JSON
```python
import json

with open("config.json") as file:
    config = json.load(file)

print(config["server"]["host"])
```

Writing:
```python
with open("output.json", "w") as file:
    json.dump(config, file, indent=2)
```

## YAML
Install PyYAML:
```bash
python3 -m pip install pyyaml
```

Read YAML:
```python
import yaml

with open("config.yaml") as file:
    config = yaml.safe_load(file)
```

Use `safe_load()` for normal configuration files.

## Example
```yaml
server:
  name: web01
  host: 192.168.1.10
  port: 80

monitoring:
  cpu_threshold: 80
  disk_threshold: 90
```

## Configuration Benefits
- Same code can run in different environments.
- Values can be changed without editing Python.
- Configuration can be version-controlled separately.
- Automation becomes easier to maintain.
