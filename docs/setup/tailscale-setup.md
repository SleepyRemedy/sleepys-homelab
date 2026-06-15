# Tailscale Setup

## Purpose

Tailscale provides secure remote access to Archer's Homelab.

The goal is to access services through a private Tailnet without exposing internal infrastructure directly to the public internet.

## Deployment

Tailscale is installed inside a dedicated LXC container.

### Container Information

LXC ID: 1000

Current Hostname:

```text id="x4i5jv"
ts-gateway
```

Previous Hostname:

```text id="hnbf8v"
charlie
```

### Operating System

Debian 13 (Trixie)

## Installation

Tailscale was installed using the official installation script:

```bash id="2ggp3f"
curl -fsSL https://tailscale.com/install.sh | sh
```

After installation, the node was connected to the Tailnet using:

```bash id="h5hlkv"
tailscale up
```

## Features

* Secure remote access
* Tailnet-based connectivity
* MagicDNS support
* Device-to-device encrypted networking

## Network Design

The homelab is designed around Tailscale as the primary remote access solution.

Services should remain accessible only through the Tailnet unless intentionally exposed in the future.

## Management

Verify the installed version:

```bash id="lfjlwm"
tailscale version
```

Check service status:

```bash id="z6i6hd"
systemctl status tailscaled
```

## Status

Operational
