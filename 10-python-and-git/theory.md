# Module 10 — Python + Git

## Objectives
- Use Git from Python.
- Inspect repository state.
- Capture Git output.
- Generate a repository report.

## Git Commands
Common commands:
```bash
git status --short
git log -1
git branch --show-current
```

## Python
```python
import subprocess

result = subprocess.run(
    ["git", "status", "--short"],
    capture_output=True,
    text=True,
    check=True
)

print(result.stdout)
```

## Automation Ideas
- Repository health checks
- Latest commit reports
- Branch reports
- Pre-deployment checks
- CI validation

Never automate destructive Git commands such as forced resets without explicit safeguards.
