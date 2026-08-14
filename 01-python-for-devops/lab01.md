# Module 01 — Python for DevOps

## Introduction

In this module, we will use Python to collect Linux system information and perform simple DevOps automation tasks.

You already know Python basics, so we will focus on **using Python in real DevOps situations**.

---

# Lab 01 — Collect Linux System Information

## 🎯 Objective

Learn how to:

- Use the `platform` module
- Use the `sys` module
- Collect Linux server information
- Display information in a readable format

## 📚 Theory

Python provides the built-in `platform` module for collecting operating-system and hardware information.

```python
import platform

print(platform.system())
print(platform.release())
print(platform.machine())
```

Possible output:

```text
Linux
6.8.0-40-generic
x86_64
```

### Useful `platform` functions

| Function | Purpose |
|---|---|
| `platform.system()` | Operating system |
| `platform.release()` | OS/kernel release |
| `platform.version()` | Detailed OS version |
| `platform.machine()` | Machine architecture |
| `platform.processor()` | Processor information |
| `platform.node()` | Hostname |

The `sys` module provides information about the Python interpreter.

```python
import sys

print(sys.version)
```

To display only the Python version:

```python
print(sys.version.split()[0])
```

## 🧩 Task

Create:

```text
system_info.py
```

The program must display:

1. Hostname
2. Operating system
3. Kernel release
4. Python version
5. Machine architecture

## 💡 Hints

Use:

```python
platform.node()
platform.system()
platform.release()
platform.machine()
sys.version.split()[0]
```

## ▶️ Expected Output

```text
===== SYSTEM INFORMATION =====
Hostname         : devops-server
Operating System : Linux
Kernel           : 6.8.0-40-generic
Python           : 3.12.3
Architecture     : x86_64
===============================
```

Actual values depend on your machine.

## ✅ Solution

```python
import platform
import sys

print("===== SYSTEM INFORMATION =====")

print("Hostname         :", platform.node())
print("Operating System :", platform.system())
print("Kernel           :", platform.release())
print("Python           :", sys.version.split()[0])
print("Architecture     :", platform.machine())

print("===============================")
```

### Solution Explanation

- `platform.node()` → hostname
- `platform.system()` → operating system
- `platform.release()` → kernel/OS release
- `sys.version.split()[0]` → Python version
- `platform.machine()` → architecture such as `x86_64`

---

# 🧪 Practice Exercise 1 — More System Information

Modify the program and additionally display:

- Processor
- Detailed OS version

## 💡 Hint

```python
platform.processor()
platform.version()
```

## ▶️ Expected Output

```text
Processor        : ...
OS Version       : ...
```

## ✅ Solution

```python
import platform
import sys

print("===== SYSTEM INFORMATION =====")

print("Hostname         :", platform.node())
print("Operating System :", platform.system())
print("Kernel           :", platform.release())
print("Python           :", sys.version.split()[0])
print("Architecture     :", platform.machine())
print("Processor        :", platform.processor())
print("OS Version       :", platform.version())

print("===============================")
```

---

# 🧪 Practice Exercise 2 — Environment Information

DevOps engineers frequently need to inspect environment variables.

## 📚 Theory

Python can access environment variables using the `os` module.

```python
import os
```

Examples:

```python
os.environ.get("HOME")
os.environ.get("USER")
os.environ.get("SHELL")
os.getcwd()
```

## 🧩 Task

Create:

```text
environment_info.py
```

Display:

- Username
- Home directory
- Shell
- PATH
- Current working directory

## 💡 Hint

Use:

```python
os.environ.get("USER")
os.environ.get("HOME")
os.environ.get("SHELL")
os.environ.get("PATH")
os.getcwd()
```

## ▶️ Expected Output

```text
===== ENVIRONMENT INFORMATION =====
Username     : justin
Home         : /home/justin
Shell        : /bin/bash
PATH         : /usr/local/bin:/usr/bin:...
Working Dir  : /home/justin/python-labs
====================================
```

## ✅ Solution

```python
import os

print("===== ENVIRONMENT INFORMATION =====")

print("Username    :", os.environ.get("USER"))
print("Home        :", os.environ.get("HOME"))
print("Shell       :", os.environ.get("SHELL"))
print("PATH        :", os.environ.get("PATH"))
print("Working Dir :", os.getcwd())

print("====================================")
```

### Why is this useful in DevOps?

The same script may run on development, testing, and production servers.

Python can automatically discover information about the environment instead of requiring an administrator to enter it manually.

That is one of the basic ideas behind **automation**.

---

# 🧪 Practice Exercise 3 — Create a Server Report

Combine the previous exercises.

Create:

```text
server_report.py
```

Display:

### System Information

- Hostname
- Operating system
- Kernel
- Architecture
- Python version

### Environment Information

- Username
- Home directory
- Shell
- Current directory

## 🎯 Requirement

Organize the output:

```text
========================================
        DEVOPS SERVER REPORT
========================================

SYSTEM INFORMATION
------------------
Hostname       :
OS             :
Kernel         :
Architecture   :
Python         :

ENVIRONMENT
-----------
Username       :
Home           :
Shell          :
Working Dir    :

========================================
```

## 💡 Recommended Approach

Build the program in small steps:

1. Import required modules
2. Collect system information
3. Collect environment information
4. Print the report

## ✅ Solution

```python
import os
import platform
import sys

print("========================================")
print("        DEVOPS SERVER REPORT")
print("========================================")

print()
print("SYSTEM INFORMATION")
print("------------------")

print("Hostname       :", platform.node())
print("OS             :", platform.system())
print("Kernel         :", platform.release())
print("Architecture   :", platform.machine())
print("Python         :", sys.version.split()[0])

print()
print("ENVIRONMENT")
print("-----------")

print("Username       :", os.environ.get("USER"))
print("Home           :", os.environ.get("HOME"))
print("Shell          :", os.environ.get("SHELL"))
print("Working Dir    :", os.getcwd())

print()
print("========================================")
```

---

# 🧪 Practice Exercise 4 — Save the Report to a File

A DevOps engineer often needs to save information instead of only displaying it on the terminal.

Modify `server_report.py` so that the report is also saved to:

```text
server_report.txt
```

## 📚 Theory — Writing to a File

Python can write data using:

```python
with open("server_report.txt", "w") as file:
    file.write("Hello")
```

`"w"` means open the file for writing.

If the file does not exist, Python creates it.

## 🧩 Task

The program must:

1. Display the report
2. Save the same report to `server_report.txt`

## 💡 Hint

Create the report as a string:

```python
report = """
SYSTEM INFORMATION
------------------
Hostname:
OS:
"""
```

Then:

```python
print(report)

with open("server_report.txt", "w") as file:
    file.write(report)
```

## ✅ Solution

```python
import os
import platform
import sys

report = f"""
========================================
        DEVOPS SERVER REPORT
========================================

SYSTEM INFORMATION
------------------
Hostname       : {platform.node()}
OS             : {platform.system()}
Kernel         : {platform.release()}
Architecture   : {platform.machine()}
Python         : {sys.version.split()[0]}

ENVIRONMENT
-----------
Username       : {os.environ.get("USER")}
Home           : {os.environ.get("HOME")}
Shell          : {os.environ.get("SHELL")}
Working Dir    : {os.getcwd()}

========================================
"""

print(report)

with open("server_report.txt", "w") as file:
    file.write(report)

print("Report saved to server_report.txt")
```

---

# 🧪 Practice Exercise 5 — Add a Timestamp

A DevOps report should normally contain the time when it was generated.

Add:

```text
Report Generated : 2026-08-14 13:20:10
```

## 💡 Hint

Use Python's `datetime` module:

```python
from datetime import datetime

datetime.now()
```

For a clean format:

```python
datetime.now().strftime("%Y-%m-%d %H:%M:%S")
```

## ✅ Solution

```python
import os
import platform
import sys
from datetime import datetime

timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")

report = f"""
========================================
        DEVOPS SERVER REPORT
========================================

Report Generated : {timestamp}

SYSTEM INFORMATION
------------------
Hostname       : {platform.node()}
OS             : {platform.system()}
Kernel         : {platform.release()}
Architecture   : {platform.machine()}
Python         : {sys.version.split()[0]}

ENVIRONMENT
-----------
Username       : {os.environ.get("USER")}
Home           : {os.environ.get("HOME")}
Shell          : {os.environ.get("SHELL")}
Working Dir    : {os.getcwd()}

========================================
"""

print(report)

with open("server_report.txt", "w") as file:
    file.write(report)

print("Report saved successfully.")
```

---

# 🎯 Mini DevOps Task — Server Information Tool

Create:

```text
server_info.py
```

The tool should generate a complete server information report containing:

### System

- Hostname
- OS
- Kernel
- Architecture
- Processor
- Python version

### Environment

- Username
- Home directory
- Shell
- Current directory

### Report

- Current date/time
- Display report on screen
- Save report to `server_info.txt`

## 🧠 Recommended Approach

Do not copy the previous solution directly.

Build the program in stages:

### Step 1

Import:

```python
import os
import platform
import sys
from datetime import datetime
```

### Step 2

Collect the values.

### Step 3

Create the report.

### Step 4

Print the report.

### Step 5

Save the report.

---

# 🚀 Final Challenge — Server Health Report

> **No solution is provided for this challenge.**

Create:

```text
health_report.py
```

The program should produce a basic health report for the Linux machine.

It should collect:

- Hostname
- Operating system
- Kernel version
- Python version
- CPU information
- Username
- Current working directory
- Current date/time

Then save the report as:

```text
health_report.txt
```

## Additional Requirements

Your program should:

1. Have a clear title.
2. Organize information into sections.
3. Use functions where appropriate.
4. Use meaningful variable names.
5. Include comments for important parts.
6. Produce clean terminal output.
7. Save the same report to a file.

## ⭐ Bonus

Add:

```text
Script execution time
```

Use:

```python
import time
```

to measure how long your program takes to execute.

---

# 📌 Module 01 — What You Learned

After completing this module, you should be comfortable using Python to:

- Collect Linux system information
- Read environment variables
- Work with the current directory
- Create text reports
- Write reports to files
- Add timestamps
- Combine multiple Python modules
- Build a small DevOps automation script

These concepts will be used repeatedly in the upcoming modules.
