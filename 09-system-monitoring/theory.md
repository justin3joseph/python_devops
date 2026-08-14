# Module 09 — System Monitoring

## Objectives
- Install and use `psutil`.
- Monitor CPU, memory and disk.
- Inspect processes.
- Build threshold-based monitoring.

Install:
```bash
python3 -m pip install psutil
```

## CPU
```python
import psutil
print(psutil.cpu_percent(interval=1))
```

## Memory
```python
memory = psutil.virtual_memory()
print(memory.percent)
```

## Disk
```python
disk = psutil.disk_usage("/")
print(disk.percent)
```

## Processes
```python
for process in psutil.process_iter(["pid", "name"]):
    print(process.info)
```

## Threshold Monitoring
```python
if disk.percent > 90:
    print("WARNING: Disk usage is high")
```

## DevOps Uses
- Server health checks
- Alerting
- Capacity reports
- Troubleshooting
- Automated remediation
