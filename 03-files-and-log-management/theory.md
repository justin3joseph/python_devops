# Module 03 — File and Directory Automation

## Objectives
- Work with files using `pathlib`.
- Copy and move files with `shutil`.
- Search files with `glob`.
- Build a simple backup workflow.

## `pathlib`
```python
from pathlib import Path

log_dir = Path("/var/log")
print(log_dir.exists())
print(log_dir.is_dir())

for file in log_dir.glob("*.log"):
    print(file)
```

## Reading Files
```python
path = Path("app.log")

with path.open() as file:
    for line in file:
        print(line.rstrip())
```

## `shutil`
```python
import shutil

shutil.copy2("app.log", "backup/app.log")
```

Other useful operations include `copytree()`, `move()` and `rmtree()`.

## Safe Automation
Before deleting or overwriting:
- Check that the path exists.
- Verify it is the expected type.
- Avoid dangerous broad paths.
- Log the operation.
- Test with sample data first.

## DevOps Uses
- Log collection
- Configuration deployment
- Backups
- Temporary-file cleanup
- Artifact management
