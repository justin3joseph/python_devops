# Module 05 — Python for DevOps: Regular Expressions for DevOps

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

# Lab 01 — Extract Numbers

## 🎯 Objective

Extract numbers from system text using regex.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Regular expressions with `re`, matching patterns, extracting values, counting matches, and redacting sensitive strings.

## 🧩 Task

Complete **Lab 01 — Extract Numbers**.

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
import re

text = "Server has 8 CPUs, 32 GB RAM and port 8080"
numbers = re.findall(r"\d+", text)

print(numbers)
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

# Lab 02 — Extract IP Addresses

## 🎯 Objective

Find IPv4 addresses in log files.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Regular expressions with `re`, matching patterns, extracting values, counting matches, and redacting sensitive strings.

## 🧩 Task

Complete **Lab 02 — Extract IP Addresses**.

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
import re
from pathlib import Path

text = Path("server.log").read_text()
pattern = r"\b(?:\d{1,3}\.){3}\d{1,3}\b"

for ip in re.findall(pattern, text):
    print(ip)
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

# Lab 03 — Analyze Failed Logins

## 🎯 Objective

Find failed-login IP addresses and count occurrences.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Regular expressions with `re`, matching patterns, extracting values, counting matches, and redacting sensitive strings.

## 🧩 Task

Complete **Lab 03 — Analyze Failed Logins**.

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
import re
from collections import Counter
from pathlib import Path

text = Path("auth.log").read_text()

pattern = r"Failed password.*from (\d{1,3}(?:\.\d{1,3}){3})"
ips = re.findall(pattern, text)

print("Total failures:", len(ips))
print("By IP:", Counter(ips))
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

# Lab 04 — Redact Sensitive Data

## 🎯 Objective

Replace passwords and tokens in text with `REDACTED`.

By completing this lab, students should understand how this technique can be used in a real DevOps automation workflow.

## 📚 Theory

### Why this matters in DevOps

DevOps scripts commonly automate repetitive server, application, configuration, monitoring, and deployment tasks. Python provides standard-library modules and widely used third-party libraries for these tasks.

### Key concepts


Regular expressions with `re`, matching patterns, extracting values, counting matches, and redacting sensitive strings.

## 🧩 Task

Complete **Lab 04 — Redact Sensitive Data**.

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
import re

text = "username=admin password=secret123 token=abc123"

text = re.sub(r"password=\S+", "password=REDACTED", text)
text = re.sub(r"token=\S+", "token=REDACTED", text)

print(text)
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
