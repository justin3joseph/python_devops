# Module 13 — Python for DevOps: Python in CI/CD

## Introduction

This module applies Python basics to practical DevOps automation.

Each lab follows the same classroom flow:

1. 🎯 Objective
2. 📚 Theory
3. 🧩 Task
4. 💡 Hints
5. ▶️ Expected Output
6. ✅ Solution
7. 🔍 Solution Explanation
8. 🧪 Student Practice
9. 🚀 Final Challenge

> **Instructor note:** The solutions are included for the practice labs. The final challenge is intentionally solution-free.


---

# Lab 01 — CI Exit Codes

## 🎯 Objective

Use Python exit codes to signal success/failure.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


CI/CD jobs depend on deterministic scripts and exit codes. A zero exit code normally means success; non-zero means failure.

## 🧩 Task

Complete **Lab 01 — CI Exit Codes**.

Start with the smallest working version. Test it, inspect the output, then improve it.

## 💡 Hints

- Break the task into small functions or steps.
- Use meaningful variable names.
- Print intermediate values while learning.
- Handle expected errors instead of allowing confusing tracebacks.
- Test both the normal case and at least one failure case.

## ▶️ Expected Output

Your output should clearly show that the requested operation completed successfully.

Example style:

```text
========================================
        DEVOPS LAB 1
========================================
Task completed successfully
Result      : <actual result>
Status      : PASS
========================================
```

Actual values will depend on the student's system.

## ✅ Solution

```python
import sys

success = True

if success:
    print("CI check passed")
    sys.exit(0)
else:
    print("CI check failed")
    sys.exit(1)
```

## 🔍 Solution Explanation

1. Import the required module(s).
2. Collect or process the required data.
3. Perform the requested automation.
4. Handle errors where appropriate.
5. Display a clear result.

Students should understand **why** each step is required, not simply copy the code.

## 🧪 Student Practice

Modify the solution to add one useful improvement.

Suggested variations:

- Add input validation.
- Add a timestamp.
- Save the result to a file.
- Add a warning threshold.
- Process multiple inputs.
- Add a command-line option.
- Handle an expected failure gracefully.

Write the improved version yourself before looking at the solution above again.


---

# Lab 02 — Validate Required Files

## 🎯 Objective

Build a simple CI validation script.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


CI/CD jobs depend on deterministic scripts and exit codes. A zero exit code normally means success; non-zero means failure.

## 🧩 Task

Complete **Lab 02 — Validate Required Files**.

Start with the smallest working version. Test it, inspect the output, then improve it.

## 💡 Hints

- Break the task into small functions or steps.
- Use meaningful variable names.
- Print intermediate values while learning.
- Handle expected errors instead of allowing confusing tracebacks.
- Test both the normal case and at least one failure case.

## ▶️ Expected Output

Your output should clearly show that the requested operation completed successfully.

Example style:

```text
========================================
        DEVOPS LAB 2
========================================
Task completed successfully
Result      : <actual result>
Status      : PASS
========================================
```

Actual values will depend on the student's system.

## ✅ Solution

```python
from pathlib import Path
import sys

required = ["app.py", "config.yaml", "README.md"]
missing = [name for name in required if not Path(name).exists()]

if missing:
    print("Missing files:", missing)
    sys.exit(1)

print("Required files are present")
sys.exit(0)
```

## 🔍 Solution Explanation

1. Import the required module(s).
2. Collect or process the required data.
3. Perform the requested automation.
4. Handle errors where appropriate.
5. Display a clear result.

Students should understand **why** each step is required, not simply copy the code.

## 🧪 Student Practice

Modify the solution to add one useful improvement.

Suggested variations:

- Add input validation.
- Add a timestamp.
- Save the result to a file.
- Add a warning threshold.
- Process multiple inputs.
- Add a command-line option.
- Handle an expected failure gracefully.

Write the improved version yourself before looking at the solution above again.


---

# Lab 03 — Python Syntax Check

## 🎯 Objective

Run a Python compilation check.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


CI/CD jobs depend on deterministic scripts and exit codes. A zero exit code normally means success; non-zero means failure.

## 🧩 Task

Complete **Lab 03 — Python Syntax Check**.

Start with the smallest working version. Test it, inspect the output, then improve it.

## 💡 Hints

- Break the task into small functions or steps.
- Use meaningful variable names.
- Print intermediate values while learning.
- Handle expected errors instead of allowing confusing tracebacks.
- Test both the normal case and at least one failure case.

## ▶️ Expected Output

Your output should clearly show that the requested operation completed successfully.

Example style:

```text
========================================
        DEVOPS LAB 3
========================================
Task completed successfully
Result      : <actual result>
Status      : PASS
========================================
```

Actual values will depend on the student's system.

## ✅ Solution

```python
import subprocess
import sys

result = subprocess.run(
    [sys.executable, "-m", "py_compile", "app.py"]
)

if result.returncode == 0:
    print("Syntax check passed")
else:
    print("Syntax check failed")

sys.exit(result.returncode)
```

## 🔍 Solution Explanation

1. Import the required module(s).
2. Collect or process the required data.
3. Perform the requested automation.
4. Handle errors where appropriate.
5. Display a clear result.

Students should understand **why** each step is required, not simply copy the code.

## 🧪 Student Practice

Modify the solution to add one useful improvement.

Suggested variations:

- Add input validation.
- Add a timestamp.
- Save the result to a file.
- Add a warning threshold.
- Process multiple inputs.
- Add a command-line option.
- Handle an expected failure gracefully.

Write the improved version yourself before looking at the solution above again.


---

# Lab 04 — API Smoke Test

## 🎯 Objective

Create a CI-friendly endpoint test.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


CI/CD jobs depend on deterministic scripts and exit codes. A zero exit code normally means success; non-zero means failure.

## 🧩 Task

Complete **Lab 04 — API Smoke Test**.

Start with the smallest working version. Test it, inspect the output, then improve it.

## 💡 Hints

- Break the task into small functions or steps.
- Use meaningful variable names.
- Print intermediate values while learning.
- Handle expected errors instead of allowing confusing tracebacks.
- Test both the normal case and at least one failure case.

## ▶️ Expected Output

Your output should clearly show that the requested operation completed successfully.

Example style:

```text
========================================
        DEVOPS LAB 4
========================================
Task completed successfully
Result      : <actual result>
Status      : PASS
========================================
```

Actual values will depend on the student's system.

## ✅ Solution

```python
import requests
import sys

try:
    response = requests.get("https://example.com", timeout=10)
    print("HTTP status:", response.status_code)
    sys.exit(0 if response.status_code == 200 else 1)
except requests.RequestException as error:
    print("Smoke test failed:", error)
    sys.exit(1)
```

## 🔍 Solution Explanation

1. Import the required module(s).
2. Collect or process the required data.
3. Perform the requested automation.
4. Handle errors where appropriate.
5. Display a clear result.

Students should understand **why** each step is required, not simply copy the code.

## 🧪 Student Practice

Modify the solution to add one useful improvement.

Suggested variations:

- Add input validation.
- Add a timestamp.
- Save the result to a file.
- Add a warning threshold.
- Process multiple inputs.
- Add a command-line option.
- Handle an expected failure gracefully.

Write the improved version yourself before looking at the solution above again.


---

# 🚀 Final Challenge — Independent Student Task

> **No solution is provided for this challenge.**

Create a small DevOps automation program that uses the concepts learned in this module.

## Requirements

1. Use Python rather than manually performing the task.
2. Accept input or configuration where appropriate.
3. Produce clear terminal output.
4. Handle at least one expected error.
5. Use functions where appropriate.
6. Use meaningful variable names.
7. Save a report or result when it makes sense.
8. Test both success and failure cases.
9. Add a short `README.md` explaining how to run the program.

## ⭐ Bonus

Add logging, command-line options, and a useful exit code.

---

# 📌 Module Summary

After completing this module, students should be able to explain the main concepts covered and apply them to a practical DevOps automation problem.

The goal is not just to write Python code, but to use Python to **automate real operational tasks reliably and repeatedly**.
