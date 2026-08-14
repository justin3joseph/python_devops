# Module 01 — Practice Solutions

## Practice 1
```python
import platform, sys
print("Hostname:", platform.node())
print("OS:", platform.system())
print("Kernel:", platform.release())
print("Python:", sys.version.split()[0])
print("Architecture:", platform.machine())
```

## Practice 2
```python
import os, platform, sys
print("Hostname:", platform.node())
print("OS:", platform.system())
print("Python:", sys.version.split()[0])
print("Architecture:", platform.machine())
print("Directory:", os.getcwd())
print("User:", os.environ.get("USER", "unknown"))
```

## Practice 3
```python
import os, platform, sys
report = "Hostname: " + platform.node() + "\n"
report += "OS: " + platform.system() + "\n"
report += "Python: " + sys.version.split()[0] + "\n"
report += "Directory: " + os.getcwd() + "\n"
print(report)
with open("server_report.txt", "w") as f:
    f.write(report)
```

## Practice 4
Add `HOME`, `SHELL`, `PATH`, processor and architecture using `os.environ` and `platform`.

## Challenge
No solution provided.
