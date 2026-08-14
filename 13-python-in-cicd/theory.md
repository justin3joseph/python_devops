# Module 13 — Python in CI/CD

## Objectives
- Understand how Python participates in CI/CD.
- Use exit codes.
- Run automated checks.
- Create deployment validation scripts.

## Pipeline Pattern
```text
Commit
  ↓
Build
  ↓
Test
  ↓
Validate
  ↓
Package
  ↓
Deploy
  ↓
Verify
```

## Python Exit Status
A CI job normally treats exit code `0` as success.

```python
import sys

if validation_failed:
    sys.exit(1)

sys.exit(0)
```

## Example Validation
```python
import requests

response = requests.get("https://example.com", timeout=10)

if response.status_code != 200:
    raise SystemExit("Application health check failed")
```

## DevOps Uses
- Unit-test execution
- Configuration validation
- API health checks
- Deployment verification
- Report generation
