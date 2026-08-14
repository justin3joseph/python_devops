# Lab 01 — System Information Reporter

## Objective
Create a Python script that reports basic Linux and Python environment information.

## Requirements
- Python 3
- Linux VM or WSL

## Tasks
1. Create `system_info.py`.
2. Display hostname.
3. Display OS/platform information.
4. Display Python version.
5. Display current working directory.
6. Display current user.
7. Format the output as a readable report.

## Starter
```python
import os
import platform
import sys

print("===== SYSTEM INFORMATION =====")
print("Hostname :", platform.node())
print("OS       :", platform.system())
print("Release  :", platform.release())
print("Python   :", sys.version.split()[0])
print("Directory:", os.getcwd())
print("User     :", os.environ.get("USER", "unknown"))
```

## Extension
Add CPU architecture and home directory.

## Questions
1. Why is Python useful for DevOps?
2. What is an environment variable?
3. Why should operational scripts be repeatable?
