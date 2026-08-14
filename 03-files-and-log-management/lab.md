# Lab 03 — Automated Log Backup

## Objective
Create a script that finds log files and copies them into a backup directory.

## Tasks
1. Create `sample_logs`.
2. Create three `.log` files.
3. Use `pathlib` to locate them.
4. Create `backup_logs`.
5. Copy files using `shutil.copy2()`.
6. Print each copied file.
7. Verify the backup.

## Challenge
Add a file-size report and skip files that have already been backed up.

## Safety
Use sample files. Do not delete or modify production logs during this exercise.

## Questions
1. Why is `pathlib` useful?
2. What is the difference between copying and moving?
3. Why should backup scripts verify the destination?
