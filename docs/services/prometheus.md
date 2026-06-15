# Prometheus

## Purpose

Prometheus collects and stores monitoring metrics for Archer's Homelab.

These metrics are visualized through Grafana dashboards.

## Deployment

Prometheus is installed directly on the Proxmox host.

The service is managed through systemd and starts automatically during boot.

## Verification

The service can be checked using:

```bash
systemctl status prometheus
```

## Components

Installed components:

* Prometheus
* Prometheus Node Exporter
* Prometheus Node Exporter Collectors

## Function

Prometheus collects metrics from the host system and stores them as time-series data.

Grafana connects to Prometheus to display dashboards and visualizations.

## Status

Operational

