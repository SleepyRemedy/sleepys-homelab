# Homepage Host Validation Issue

## Problem

Homepage was accessible through its IP address but rejected requests when accessed through a custom hostname.

The dashboard displayed a host validation error and refused to load.

## Symptoms

* Homepage container was running normally
* Service was reachable on the configured port
* Access through a custom hostname failed
* Homepage rejected incoming requests

## Investigation

The Homepage container logs were inspected.

Environment variables and container configuration were reviewed using commands such as:

```bash id="q6gdyf"
docker logs homepage
```

```bash id="4sq57r"
docker inspect homepage
```

Additional checks were performed on the Docker Compose configuration.

## Root Cause

Homepage validates incoming host headers for security reasons.

The desired hostname was not included in the allowed host configuration.

As a result, Homepage rejected requests using that hostname.

## Solution

The Docker Compose configuration was updated to allow the required hostname.

Homepage was redeployed after updating the container configuration.

## Result

Homepage successfully accepted requests from the desired hostname.

The dashboard became accessible through the configured address.

## Lessons Learned

* Some web applications validate incoming host headers.
* Container logs are often the fastest way to identify application-level issues.
* Docker environment variables can directly affect application accessibility.
