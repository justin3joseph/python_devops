# Module 01 — Python for DevOps

## Objectives
- Understand where Python fits in DevOps.
- Distinguish manual administration from automation.
- Build small operational scripts.
- Collect Linux system information.

## 1. Python in DevOps
DevOps requires repetitive tasks to be reliable and repeatable. Python is useful for automation because it has a readable syntax and a large ecosystem.

Typical uses:
- Linux administration
- Log processing
- Monitoring
- API automation
- Cloud automation
- Docker automation
- CI/CD scripts
- Backup and reporting

## 2. Automation Mindset
A good automation script should be:
1. Repeatable
2. Predictable
3. Safe
4. Logged
5. Easy to troubleshoot

Avoid hard-coding passwords, deleting data without checks, or running privileged commands unnecessarily.

## 3. Common DevOps Python Libraries
| Library | Purpose |
|---|---|
| `os` | OS/environment operations |
| `sys` | Python runtime and arguments |
| `pathlib` | File paths |
| `subprocess` | Run system commands |
| `shutil` | File operations |
| `re` | Regular expressions |
| `json` | JSON data |
| `logging` | Application logs |
| `argparse` | CLI applications |
| `requests` | HTTP APIs |
| `psutil` | System monitoring |
| `boto3` | AWS automation |

## 4. First DevOps Script
A useful first script reports:
- Hostname
- Operating system
- Python version
- Current directory
- Current user

## Key Takeaways
Python for DevOps is mainly about **automation**, not advanced Python syntax. The goal is to turn repetitive operational tasks into reliable scripts.
