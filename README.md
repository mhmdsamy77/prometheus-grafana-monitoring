# Prometheus and Grafana Monitoring

A Linux server monitoring stack using Prometheus, Grafana, Node Exporter, and Docker Compose.

## Project Overview

This project monitors Linux system metrics using a containerized monitoring stack.

## Architecture

The project consists of three services:

- **Prometheus:** Collects and stores monitoring metrics.
- **Node Exporter:** Exposes Linux system metrics such as CPU, memory, and disk usage.
- **Grafana:** Visualizes metrics through dashboards.

Docker Compose manages all services.

## Technologies Used

- Linux
- Docker
- Docker Compose
- Prometheus
- Grafana
- Node Exporter

## Project Structure

```text
prometheus-grafana-monitoring/
├── prometheus/
│   └── prometheus.yml
├── docker-compose.yml
├── .gitignore
├── LICENSE
└── README.md
```

## Run the Project

Start the monitoring stack:

```bash
docker compose up -d
```

Check running containers:

```bash
docker compose ps
```

## Access the Services

- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000
- Node Exporter: http://localhost:9100/metrics

## Grafana Setup

Log in to Grafana using the initial credentials:

- Username: admin
- Password: admin

Then add Prometheus as a data source using:

```text
http://prometheus:9090
```

## Data Persistence

Docker named volumes are used to preserve Prometheus and Grafana data when containers are removed.

## Author

Mohamed Samy
