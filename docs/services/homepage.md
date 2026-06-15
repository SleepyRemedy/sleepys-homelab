# Homepage Dashboard

## Purpose

Homepage serves as the central dashboard of Archer's Homelab.

It provides quick access to infrastructure services, monitoring tools and external resources through a single interface.

## Deployment

Homepage is deployed inside the dedicated Docker LXC container.

Container:

* LXC ID: 100
* Hostname: homepage

Docker Image:

```text
ghcr.io/gethomepage/homepage:latest
```

## Configuration

Homepage is configured using YAML files located under:

```text
/opt/docker/homepage/config
```

Key configuration files:

```text
settings.yaml
services.yaml
docker.yaml
custom.css
```

## Services

Current dashboard entries include:

* Proxmox VE
* Grafana
* Prometheus
* Tailscale
* Cloudflare
* GitHub

## Customization

The dashboard was customized to match the visual style of Archer's Homelab.

Customizations include:

* Custom background image
* Glassmorphism-inspired interface
* Transparent service cards
* Blur effects
* Custom CSS styling

## Challenges Encountered

Several issues were encountered during deployment and customization.

### Background Image

The custom background image initially failed to load correctly.

### Host Validation

Homepage initially rejected requests from custom hostnames.

### User Interface Styling

Multiple CSS iterations were required before achieving the desired glassmorphism appearance.
## Result

Homepage now serves as the primary entry point for Archer's Homelab and provides a centralized overview of infrastructure and services.

## Related Troubleshooting

- [Homepage Background Image Issue](../troubleshooting/homepage-background-image.md)
- [Homepage Host Validation Issue](../troubleshooting/homepage-host-validation.md)
- [Homepage Glassmorphism UI Customization](../troubleshooting/homepage-glassmorphism-ui.md)


## Status

Operational
