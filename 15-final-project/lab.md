# Lab 15 — Final Project: Python DevOps Automation Toolkit

## Objective
Build a practical, GitHub-hosted Python DevOps toolkit.

## Required Commands
```bash
python devops.py system
python devops.py monitor
python devops.py logs ./sample_logs
python devops.py backup ./sample_logs ./backup
python devops.py api https://example.com
python devops.py docker
```

## Requirements
- Use `argparse`.
- Organize functionality into modules.
- Use YAML/JSON configuration where appropriate.
- Add exception handling.
- Add Python logging.
- Validate input.
- Add at least five automated tests.
- Document installation and usage.
- Store the project in Git.
- Include `requirements.txt`.

## Suggested Structure
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

## Project Workflow
1. Create a Git repository.
2. Implement one feature at a time.
3. Test each feature.
4. Commit meaningful changes.
5. Document installation and commands.
6. Demonstrate the project on a Linux VM.
7. Explain safety considerations.

## Assessment
| Area | Marks |
|---|---:|
| Python implementation | 15 |
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
