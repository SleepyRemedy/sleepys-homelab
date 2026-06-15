# IPv6 Network Issue

## Problem

After installing Proxmox VE, package updates failed.

Running:

```bash
apt update
```

resulted in network-related errors, including:

```text
Network is unreachable
```

This prevented the system from downloading packages and updates from the configured repositories.

## Investigation

The issue occurred during the initial setup phase before the web interface was used.

Troubleshooting was performed directly from the Proxmox host terminal.

The problem appeared to be related to the network configuration and repository connectivity.

## Solution

The network configuration was reviewed and adjusted.

The following file was modified:

```bash
/etc/network/interfaces
```

Changes included reviewing the bridge configuration (`vmbr0`), network interfaces and DNS settings until stable connectivity was restored.

Sensitive network information has been omitted from this documentation.

## Result

Network connectivity was restored and package repositories became reachable.

The following command completed successfully:

```bash
apt update
```

The system was then ready for further configuration and updates.

## Lessons Learned

* Verify network connectivity immediately after installation.
* Test repository access before proceeding with additional configuration.
* Initial setup issues are often easier to diagnose directly from the host terminal than through the web interface.
