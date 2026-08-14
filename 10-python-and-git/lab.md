# Lab 10 — Git Repository Reporter

## Objective
Create a Python script that reports the current Git repository state.

## Tasks
1. Create a Git repository.
2. Add sample files.
3. Make at least two commits.
4. Write `git_report.py`.
5. Use `subprocess` to run:
```text
git branch --show-current
git log -1 --oneline
git status --short
```
6. Print the results.

## Challenge
Write the report to `git_report.txt`.

## Questions
1. Why is Git important for DevOps scripts?
2. Why should scripts avoid destructive Git operations by default?
