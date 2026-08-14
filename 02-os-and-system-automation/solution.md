# Module 02 — Practice Solutions

## Practice 1
```python
import os
print(os.getcwd())
print(os.listdir("/tmp"))
print(os.listdir("/var/log"))
```

## Practice 2
```python
import os
for name in ["HOME", "USER", "SHELL", "PATH"]:
    print(name, "=", os.environ.get(name))
```

## Practice 3
```python
import os
for d in ["devops_lab/logs", "devops_lab/backup", "devops_lab/reports"]:
    os.makedirs(d, exist_ok=True)
```

## Practice 4
```python
import os, sys
if len(sys.argv) != 2:
    print("Usage: python inspect.py <directory>")
    sys.exit(1)
path = sys.argv[1]
if not os.path.isdir(path):
    print("Directory does not exist")
    sys.exit(1)
print("Entries:", len(os.listdir(path)))
```

## Practice 5
```python
import platform
print(platform.system())
print(platform.release())
print(platform.machine())
print(platform.processor())
print(platform.python_version())
```

## Challenge
No solution provided.
