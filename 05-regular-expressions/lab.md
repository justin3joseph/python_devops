# Lab 05 — Authentication Log Analyzer

## Objective
Use regex to extract useful information from a sample authentication log.

## Sample Data
Create `auth_sample.log`:
```text
Aug 14 09:10 server sshd[1001]: Failed password for user from 192.168.1.25
Aug 14 09:11 server sshd[1002]: Failed password for user from 10.0.0.15
Aug 14 09:12 server sshd[1003]: Accepted password for admin from 192.168.1.20
```

## Tasks
1. Find all IP addresses.
2. Count failed login lines.
3. Extract usernames if present.
4. Print a summary.

## Challenge
Use `collections.Counter` to find the most frequent source IP.

## Note
Regex can find IPv4-looking strings. Use Python's `ipaddress` module when strict address validation is required.
