# Module 02 — `os`, `sys` and `platform`

## Objectives
- Use `os` for operating-system operations.
- Read environment variables.
- Use `sys` for runtime information and arguments.
- Identify OS and hardware information with `platform`.

## `os`
Useful functions:
```python
import os

print(os.getcwd())
print(os.listdir("."))
print(os.environ.get("HOME"))
os.makedirs("backup", exist_ok=True)
```

## Environment Variables
Environment variables are useful for configuration:
```python
import os
user = os.environ.get("USER")
home = os.environ.get("HOME")
```

Do not store passwords directly in source code.

## `sys`
```python
import sys

print(sys.version)
print(sys.platform)
print(sys.argv)
```

`sys.argv` contains command-line arguments.

## `platform`
```python
import platform

print(platform.system())
print(platform.release())
print(platform.machine())
print(platform.processor())
```

## DevOps Applications
These modules are useful when scripts need to:
- Detect the current environment
- Find configuration directories
- Read environment variables
- Build portable scripts
- Inspect the host
