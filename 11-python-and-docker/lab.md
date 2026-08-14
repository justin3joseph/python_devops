# Lab 11 — Docker Container Reporter

## Objective
Use Python to inspect Docker containers.

## Option A — Docker CLI
Run through Python:
```bash
docker ps --format "{{.Names}} {{.Status}}"
```

## Option B — Docker SDK
Install:
```bash
python3 -m pip install docker
```

## Tasks
1. Run a test container.
2. List running containers.
3. Display name and status.
4. Stop the test container.
5. Verify the status.

## Challenge
Create a report showing both running and stopped containers.

## Safety
Do not automatically remove containers or images on a production Docker host.
