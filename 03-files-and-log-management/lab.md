# Module 03 — Python for DevOps: Files and Log Management

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

# Lab 01 — Read a Log File

## 🎯 Objective

Read a log file line by line and summarize it.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Reading files with `open()`, `pathlib.Path`, line processing, file matching, copying, and basic log analysis.

## 🧩 Task

Complete **Lab 01 — Read a Log File**.

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
from pathlib import Path

path = Path("server.log")
for number, line in enumerate(path.read_text().splitlines(), 1):
    print(f"{number:04d}: {line}")
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

# Lab 02 — Find Log Files

## 🎯 Objective

Use `pathlib` to find `.log` files.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Reading files with `open()`, `pathlib.Path`, line processing, file matching, copying, and basic log analysis.

## 🧩 Task

Complete **Lab 02 — Find Log Files**.

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

for log in Path("logs").glob("*.log"):
    print(log)
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

# Lab 03 — Copy Log Backups

## 🎯 Objective

Create a backup directory and copy log files.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Reading files with `open()`, `pathlib.Path`, line processing, file matching, copying, and basic log analysis.

## 🧩 Task

Complete **Lab 03 — Copy Log Backups**.

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
from pathlib import Path
import shutil

source = Path("logs")
backup = Path("backup")
backup.mkdir(exist_ok=True)

for log in source.glob("*.log"):
    shutil.copy2(log, backup / log.name)

print("Log backup completed.")
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

# Lab 04 — Log Statistics

## 🎯 Objective

Count lines, errors and warnings.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Reading files with `open()`, `pathlib.Path`, line processing, file matching, copying, and basic log analysis.

## 🧩 Task

Complete **Lab 04 — Log Statistics**.

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
from pathlib import Path

text = Path("server.log").read_text().splitlines()
errors = sum("ERROR" in line for line in text)
warnings = sum("WARNING" in line for line in text)

print("Lines   :", len(text))
print("Errors  :", errors)
print("Warnings:", warnings)
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
