# Module 09 — Python for DevOps: System Monitoring

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

# Lab 01 — CPU Monitoring

## 🎯 Objective

Read CPU usage with `psutil`.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


`psutil` for CPU, memory, disk, and process information; thresholds and health checks.

## 🧩 Task

Complete **Lab 01 — CPU Monitoring**.

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
import psutil

cpu = psutil.cpu_percent(interval=1)
print("CPU usage:", cpu, "%")
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

# Lab 02 — Memory Monitoring

## 🎯 Objective

Collect memory usage and percentages.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


`psutil` for CPU, memory, disk, and process information; thresholds and health checks.

## 🧩 Task

Complete **Lab 02 — Memory Monitoring**.

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
import psutil

memory = psutil.virtual_memory()

print("Total :", memory.total)
print("Used  :", memory.used)
print("Free  :", memory.available)
print("Usage :", memory.percent, "%")
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

# Lab 03 — Disk Monitoring

## 🎯 Objective

Check disk capacity and usage.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


`psutil` for CPU, memory, disk, and process information; thresholds and health checks.

## 🧩 Task

Complete **Lab 03 — Disk Monitoring**.

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
import psutil

disk = psutil.disk_usage("/")

print("Total :", disk.total)
print("Used  :", disk.used)
print("Free  :", disk.free)
print("Usage :", disk.percent, "%")
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

# Lab 04 — Process Monitoring

## 🎯 Objective

List running processes.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


`psutil` for CPU, memory, disk, and process information; thresholds and health checks.

## 🧩 Task

Complete **Lab 04 — Process Monitoring**.

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
import psutil

for process in psutil.process_iter(["pid", "name", "username"]):
    try:
        print(process.info)
    except (psutil.NoSuchProcess, psutil.AccessDenied):
        pass
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

# Lab 05 — Build a Health Check

## 🎯 Objective

Combine CPU, memory and disk thresholds.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


`psutil` for CPU, memory, disk, and process information; thresholds and health checks.

## 🧩 Task

Complete **Lab 05 — Build a Health Check**.

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
        DEVOPS LAB 5
========================================
Task completed successfully
Result      : <actual result>
Status      : PASS
========================================
```

Actual values will depend on the student's system.

## ✅ Solution

```python
import psutil

cpu = psutil.cpu_percent(interval=1)
memory = psutil.virtual_memory().percent
disk = psutil.disk_usage("/").percent

print("CPU   :", cpu)
print("Memory:", memory)
print("Disk  :", disk)

if cpu > 80:
    print("WARNING: high CPU")
if memory > 80:
    print("WARNING: high memory")
if disk > 90:
    print("WARNING: high disk usage")
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
