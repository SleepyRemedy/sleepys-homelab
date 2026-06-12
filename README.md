# Archer's Homelab

> Personal homelab built to gain hands-on experience in systems administration, virtualization, monitoring, networking and containerization.

---

## Overview

This homelab serves as a practical learning environment alongside my training as an IT Specialist for System Integration (Fachinformatiker für Systemintegration).

The goal is to build, operate and troubleshoot real infrastructure while gaining experience with modern technologies used in professional IT environments.

---

## Hardware

```text
CPU    : Intel Core i7-10700K
RAM    : 32 GB
GPU    : NVIDIA RTX 3070
Storage: 256 GB SSD (Proxmox VE)
         1 TB NVMe SSD
```

---

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

---

## Current Architecture

```text
Physical Server
│
└── Proxmox VE
    │
    ├── LXC: fred
    │   ├── Grafana
    │   └── Prometheus
    │
    └── LXC: docker
        │
        └── Docker
            └── Homepage Dashboard
```

---

## Documentation

### Setup

* Proxmox Installation
* Tailscale Setup

### Services

* Grafana
* Prometheus
* Homepage Dashboard

### Troubleshooting

* IPv6 Network Issue
* Proxmox Repository Fix
* Homepage Host Validation
* NVIDIA Driver Initialization

---

## Roadmap

* [x] Proxmox VE
* [x] Grafana
* [x] Prometheus
* [x] Tailscale
* [x] Wake-on-LAN
* [x] Docker
* [x] Homepage Dashboard
* [ ] Uptime Kuma
* [ ] Reverse Proxy
* [ ] Cloudflare Tunnel
* [ ] Nextcloud
* [ ] GPU Passthrough
* [ ] Local AI Infrastructure

---

## Lessons Learned

This repository documents both successful deployments and troubleshooting experiences encountered during the development of the homelab.

The focus is not only on building services, but also on understanding how infrastructure works and how problems are diagnosed and resolved.
