# Grafana

## Purpose

Grafana serves as the primary monitoring dashboard in Archer's Homelab.

It provides visualization of system metrics collected by Prometheus.

## Deployment

Grafana is installed directly on the Proxmox host.

The service is managed through systemd and starts automatically during boot.

## Verification

The service can be checked using:

```bash
systemctl status grafana-server
```

## Current Version

Grafana 13.0.2

## Data Source

Grafana uses Prometheus as its primary metrics source.

## Status

Operational

