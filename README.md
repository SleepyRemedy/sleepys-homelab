# Sleepy's Homelab

Personal homelab built to gain hands-on experience in systems administration, virtualization, monitoring, networking and containerization.

## Overview

This homelab serves as a hands-on environment for learning and experimenting with modern infrastructure technologies.

The goal is to build, operate and troubleshoot real infrastructure while gaining practical experience with technologies commonly used in professional IT environments.

## Hardware

```text
CPU    : Intel Core i7-10700K
RAM    : 32 GB
GPU    : NVIDIA RTX 3070
Storage: 256 GB SSD (Proxmox VE)
         1 TB NVMe SSD
```

## Current Technology Stack

### Infrastructure

* Proxmox VE
* Debian Linux
* LXC Containers
* Docker

### Monitoring

* Grafana
* Prometheus

### Networking

* Tailscale
* Cloudflare

### Services

* Homepage Dashboard

## Current Architecture

```text
Physical Server
│
└── Proxmox VE
    │
    ├── Monitoring
    │   ├── Grafana
    │   └── Prometheus
    │
    ├── LXC: ts-gateway
    │   └── Tailscale
    │
    └── LXC: homepage
        │
        └── Docker
            └── Homepage Dashboard
```

## Documentation

### Setup

* [Proxmox Installation](docs/setup/proxmox-installation.md)
* [Tailscale Setup](docs/setup/tailscale-setup.md)
* [Cloudflare Setup](docs/setup/cloudflare-setup.md)

### Services

* [Docker](docs/services/docker.md)
* [Grafana](docs/services/grafana.md)
* [Prometheus](docs/services/prometheus.md)
* [Homepage Dashboard](docs/services/homepage.md)
* [Why Private Services](docs/services/why-private-services.md)

### Troubleshooting

#### Proxmox

* [IPv6 Network Issue](docs/troubleshooting/ipv6-network-issue.md)
* [Proxmox Repository Fix](docs/troubleshooting/proxmox-repository-fix.md)

#### Homepage

* [Homepage Background Image Issue](docs/troubleshooting/homepage-background-image.md)
* [Homepage Host Validation Issue](docs/troubleshooting/homepage-host-validation.md)
* [Homepage Glassmorphism UI Customization](docs/troubleshooting/homepage-glassmorphism-ui.md)

#### Hardware

* [NVIDIA GPU Compatibility Issue](docs/troubleshooting/nvidia-gpu-compatibility-issue.md)

### Projects

* [Project REMI](docs/projects/project-remi.md)
* [Wake-on-LAN](docs/projects/wake-on-lan.md)

### Architecture

* [Work in Progress](docs/architecture/wip)

## Roadmap

* [x] Proxmox VE

* [x] Grafana

* [x] Prometheus

* [x] Tailscale

* [x] Docker

* [x] Homepage Dashboard

* [x] Cloudflare

* [ ] Wake-on-LAN Dashboard Integration

* [ ] Uptime Kuma

* [ ] Reverse Proxy

* [ ] GPU Passthrough

* [ ] Local AI Infrastructure

* [ ] Project REMI

## Lessons Learned

This repository documents both successful deployments and troubleshooting experiences encountered throughout the development of the homelab.

The focus is not only on building services, but also on understanding how infrastructure works, how problems are diagnosed and how solutions are implemented.
