# Module 04 — Python + Linux Commands

## Objectives
- Execute Linux commands from Python.
- Capture standard output and errors.
- Check return codes.
- Build Linux administration scripts.

## `subprocess.run()`
```python
import subprocess

result = subprocess.run(
    ["df", "-h"],
    capture_output=True,
    text=True
)

print(result.stdout)
print(result.returncode)
```

## Standard Error
```python
if result.returncode != 0:
    print(result.stderr)
```

## Why Prefer Argument Lists?
Prefer:
```python
subprocess.run(["ls", "-l", "/tmp"])
```

rather than constructing shell commands from untrusted user input.

`subprocess.run(..., shell=True)` can be dangerous when input is not trusted.

## Useful Commands
Examples:
- `df -h`
- `free -h`
- `uptime`
- `ps`
- `ip addr`
- `systemctl status`
- `hostname`

## DevOps Pattern
A Python script can:
1. Run a command.
2. Capture its output.
3. Parse the result.
4. Decide whether action is required.
5. Log the result.
