# Module 07 — Command-Line DevOps Tools

## Objectives
- Understand command-line arguments.
- Use `argparse`.
- Create reusable DevOps utilities.
- Provide help and validation.

## Basic Example
```python
import argparse

parser = argparse.ArgumentParser(description="Server health checker")
parser.add_argument("--disk", action="store_true")
parser.add_argument("--memory", action="store_true")

args = parser.parse_args()

if args.disk:
    print("Checking disk...")
```

## CLI Design
Good CLI tools should:
- Have clear help text.
- Validate input.
- Return meaningful exit codes.
- Print useful errors.
- Avoid destructive defaults.

Example:
```bash
python server_check.py --disk
python server_check.py --memory
python server_check.py --all
```

## Exit Codes
Conventionally:
- `0` = success
- Non-zero = failure

Example:
```python
raise SystemExit(1)
```

## DevOps Uses
CLI tools can become reusable internal utilities for administrators and automation pipelines.
