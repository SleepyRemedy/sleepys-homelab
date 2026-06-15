# Homepage Background Image Issue

## Problem

A custom background image was added to the Homepage Dashboard but failed to appear.

Despite the image existing on disk, the dashboard continued to display the default background.

## Symptoms

* Background image not visible
* Homepage loaded normally
* No obvious configuration errors
* Direct image requests returned 404 errors

Example:

```text id="sgg7qj"
404 Not Found
```

## Investigation

Multiple areas were investigated:

### Configuration Files

The following files were reviewed:

```text id="hdkhsu"
settings.yaml
custom.css
docker-compose.yml
```

### Container File Structure

The Homepage container was inspected to verify whether the image existed inside the running container.

Commands used included:

```bash id="72lp66"
docker exec homepage ls -lah /app/public
```

and

```bash id="p7yjnl"
docker exec homepage ls -lah /app/config/images
```

### Web Access Test

The image was tested directly through the web server.

Requests returned:

```text id="g7tgo5"
404 Not Found
```

indicating that Homepage was not serving the image correctly.

## Root Cause

The image file existed but was not located in a path that Homepage could serve through the web interface.

As a result, Homepage could not access the image when referenced from the configuration.

## Solution

The image was copied into a location accessible by Homepage.

File locations inside the container were reviewed and adjusted until the image became available through the web interface.

Additional CSS customization was also performed to ensure the image displayed correctly as the dashboard background.

## Result

The custom background image loaded successfully.

Homepage displayed the intended custom background and later became the foundation for the glassmorphism-style interface.

## Lessons Learned

* Verify both host and container file locations.
* A file existing on disk does not guarantee it is accessible through the web application.
* Directly testing image URLs can quickly identify serving issues.
* Container file paths and application file paths may differ.
