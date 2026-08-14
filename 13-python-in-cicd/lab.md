# Lab 13 — CI Validation Script

## Objective
Create a Python validation script suitable for a CI/CD pipeline.

## Tasks
1. Create `validate.py`.
2. Check that required files exist.
3. Validate a configuration file.
4. Perform an HTTP health check.
5. Exit `0` if all checks pass.
6. Exit non-zero if any check fails.

## Example
```bash
python validate.py
echo $?
```

## Expected Behavior
A CI system can use the exit code to determine whether the stage passes.

## Challenge
Add unit tests for each validation function and make the pipeline fail when a test fails.
