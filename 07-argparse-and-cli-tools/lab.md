# Lab 07 — Build `server_check.py`

## Objective
Create a reusable command-line server checking utility.

## Required Commands
```bash
python server_check.py --disk
python server_check.py --memory
python server_check.py --all
```

## Tasks
1. Create an `argparse.ArgumentParser`.
2. Add `--disk`, `--memory` and `--all`.
3. Use `psutil` for metrics.
4. Print clear results.
5. Return exit code `0` for successful checks.
6. Implement `--help`.

## Challenge
Add:
```bash
python server_check.py --disk --threshold 90
```

## Expected Result
The program behaves like a small reusable Linux administration utility.
