# Docker LXC

## Purpose

A dedicated LXC container was created to host Docker workloads inside Archer's Homelab.

The first deployed service was the Homepage Dashboard.

## Container Information

LXC ID: 100

Hostname:

homepage

Operating System:

Debian 12 (Bookworm)

Resources:

* 2 CPU Cores
* 4 GB RAM
* 20 GB Storage

## Docker Installation

Docker was installed using the official installation script:

```bash
curl -fsSL https://get.docker.com | sh
```

## Verification

The installation was verified using:

```bash
docker run hello-world
```

## Directory Structure

The Homepage deployment was created under:

```text
/opt/docker/homepage
```

## First Service

The first Docker-based service deployed in the homelab was:

Homepage Dashboard

using Docker Compose.

## Status

Operational
