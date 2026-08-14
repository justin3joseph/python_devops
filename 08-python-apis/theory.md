# Module 08 — Python REST API Automation

## Objectives
- Understand REST API basics.
- Make HTTP requests using `requests`.
- Process JSON responses.
- Handle timeouts and errors.

Install:
```bash
python3 -m pip install requests
```

## GET Request
```python
import requests

response = requests.get(
    "https://httpbin.org/get",
    timeout=10
)

print(response.status_code)
print(response.json())
```

## POST Request
```python
payload = {"name": "web01"}

response = requests.post(
    "https://httpbin.org/post",
    json=payload,
    timeout=10
)
```

## Error Handling
```python
response.raise_for_status()
```

Always use a timeout for network automation.

## DevOps Uses
- Health checks
- Cloud APIs
- Monitoring APIs
- Ticketing systems
- Webhooks
- CI/CD integrations
