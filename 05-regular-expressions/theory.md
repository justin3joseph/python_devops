# Module 05 — Regular Expressions

## Objectives
- Understand regex patterns.
- Use Python's `re` module.
- Extract information from logs.
- Replace or validate text.

## Common Functions
```python
import re

re.search(pattern, text)
re.findall(pattern, text)
re.sub(pattern, replacement, text)
```

## Example: IP Address Extraction
```python
import re

text = "Failed login from 192.168.1.25"
ips = re.findall(r"\b(?:\d{1,3}\.){3}\d{1,3}\b", text)
print(ips)
```

The pattern identifies IPv4-looking strings. For strict validation, use `ipaddress` rather than relying only on regex.

## Example: HTTP Status
```python
codes = re.findall(r'\b(?:200|301|302|400|401|403|404|500|502|503)\b', log)
```

## DevOps Uses
- Log analysis
- Extracting IPs
- Finding errors
- Parsing deployment output
- Detecting patterns in monitoring data
