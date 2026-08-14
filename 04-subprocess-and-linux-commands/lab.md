# Lab 04 — Linux Health Checker

## Objective
Use Python to execute Linux commands and create a health report.

## Commands
Run:
```text
hostname
uptime
df -h /
free -h
```

## Tasks
1. Execute each command using `subprocess.run()`.
2. Capture output.
3. Check the return code.
4. Print errors when a command fails.
5. Format the result as a report.

## Challenge
Create:
```python
run_command(command)
```
that returns output and success status.

## Safety
Prefer argument lists and avoid constructing shell commands from untrusted input.
