# Ignition Docker

A Docker Compose setup for running Inductive Automation's Ignition SCADA platform.

## Services

### Ignition Gateway
- **Image**: `inductiveautomation/ignition:latest`
- **Ports**: 
  - 8088:8088 (Gateway web interface)
  - 8043:8043 (HTTPS)
  - 8060:8060 (Gateway control)
  - 62541:62541 (OPC UA)
- **Memory**: 4GB max, 512MB initial

## Quick Start

```bash
# Start all services
docker-compose up -d

# Stop all services
docker-compose down
```

## Configuration

- Edit `ignition/docker-compose.yml` to modify environment variables
- All data is persisted in Docker volumes
- Services restart automatically unless stopped manually

## Access Points

- Ignition Gateway: http://localhost:8088
