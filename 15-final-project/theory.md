# Module 15 — Final Project: DevOps Automation Toolkit

## Project Goal
Build a reusable Python DevOps Automation Toolkit combining Linux automation, monitoring, logs, APIs, Docker, configuration, CLI design and testing.

## Core Features
- System information
- CPU, memory and disk monitoring
- Log analysis
- File backup
- API health checks
- Docker inventory
- YAML configuration
- CLI commands
- Logging and exception handling
- Automated tests
- Git version control

## Suggested Architecture
```text
devops_toolkit/
├── devops.py
├── config.yaml
├── requirements.txt
├── README.md
├── modules/
│   ├── system.py
│   ├── monitor.py
│   ├── logs.py
│   ├── backup.py
│   ├── api.py
│   └── docker_ops.py
└── tests/
```

## Expected CLI
```bash
python devops.py system
python devops.py monitor
python devops.py logs ./sample_logs
python devops.py backup ./sample_logs ./backup
python devops.py api https://example.com
python devops.py docker
```

## Assessment
| Area | Marks |
|---|---:|
| Python/code quality | 15 |
| Linux automation | 15 |
| Monitoring | 15 |
| Log processing | 10 |
| API automation | 10 |
| CLI/configuration | 10 |
| Error handling/logging | 10 |
| Git/documentation | 5 |
| Testing | 5 |
| Safe automation | 5 |
| **Total** | **100** |
