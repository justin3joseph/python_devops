# Lab 09 — System Monitoring Tool

## Objective
Build a monitoring script using `psutil`.

## Monitor
- CPU percentage
- Memory percentage
- Disk percentage
- Number of processes

## Tasks
1. Install `psutil`.
2. Create `monitor.py`.
3. Print all metrics.
4. Add configurable thresholds.
5. Print `WARNING` when a threshold is exceeded.

## Example
```text
CPU Usage    : 32%
Memory Usage : 64%
Disk Usage   : 71%
Processes    : 180
Status       : OK
```

## Challenge
Run the monitor every 10 seconds for five iterations and write the results to `monitor.log`.
