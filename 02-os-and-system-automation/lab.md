# Lab 02 — Linux Environment Inspector

## Objective
Use `os`, `sys` and `platform` to inspect a Linux system.

## Tasks
1. Print the current directory.
2. List files in the current directory.
3. Display `HOME`, `USER` and `PATH`.
4. Display OS and kernel information.
5. Accept an optional directory from `sys.argv`.
6. Report whether the directory exists.

## Example
```bash
python system_inspector.py /var/log
```

## Challenge
Create a directory called `devops_lab` only if it does not already exist.

## Expected Result
The script identifies the selected directory and environment details without crashing when a directory is missing.
