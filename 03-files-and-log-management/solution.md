# Module 03 — Practice Solutions

## Practice 1
```python
from pathlib import Path
lines = Path("server.log").read_text().splitlines()
print("Lines:", len(lines))
for line in lines:
    print(line)
```

## Practice 2
```python
from pathlib import Path
for p in Path("logs").glob("*.log"):
    print(p)
```

## Practice 3
```python
from pathlib import Path
import shutil
src, dst = Path("logs"), Path("backup")
dst.mkdir(exist_ok=True)
for p in src.glob("*.log"):
    shutil.copy2(p, dst / p.name)
```

## Practice 4
```python
from pathlib import Path
p = Path("logs/app.log")
print("Exists:", p.exists())
if p.exists():
    print("Size:", p.stat().st_size)
```

## Practice 5
```python
from pathlib import Path
import shutil
src, dst = Path("logs"), Path("backup")
dst.mkdir(exist_ok=True)
count = 0
for p in src.glob("*.log"):
    shutil.copy2(p, dst / p.name)
    count += 1
print("Copied:", count)
```

## Challenge
No solution provided.
