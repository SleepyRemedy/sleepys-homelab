# Wake-on-LAN

## Purpose

Wake-on-LAN (WoL) is used to remotely power on the homelab server when it is not running.

This allows the server to remain powered off when not needed, reducing energy consumption while still providing convenient remote access when required.

## Current Implementation

Wake-on-LAN is currently performed from a Windows workstation using:

```text
WakeOnLanGui.exe
```

The application sends a Wake-on-LAN magic packet to the server's network adapter, causing the machine to power on.

## Current Workflow

```text
Server Off
↓
Open WakeOnLanGui.exe
↓
Send Magic Packet
↓
Server Starts
```

While simple, this approach is reliable and requires minimal maintenance.

## Future Idea

A future goal is to integrate Wake-on-LAN into the homelab dashboard experience.

The desired workflow would be:

```text
Server Off
↓
Open Dashboard
↓
Press "Start Server"
↓
Wake-on-LAN Packet Sent
↓
Server Starts
```

## Technical Consideration

The current Homepage Dashboard runs on the same physical server that it would be responsible for waking.

As a result, dashboard-based Wake-on-LAN is not possible while the server is powered off.

To support this feature, an additional always-on device would be required, such as:

* Raspberry Pi
* Mini PC
* NAS
* Router with Wake-on-LAN capabilities

The always-on device would host the dashboard or a lightweight management service capable of sending Wake-on-LAN packets.

## Status

Current Solution:

✅ Operational

Future Dashboard Integration:

🔄 Planned

## Lessons Learned

* The simplest solution is often sufficient.
* Wake-on-LAN is extremely useful in homelab environments.
* Dashboard-based power management requires infrastructure that remains online even when the main server is powered off.
