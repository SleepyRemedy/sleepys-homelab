# Cloudflare Setup

## Purpose

Cloudflare is used for DNS management and secure access to selected homelab services.

The goal is to simplify service access while maintaining control over which services are exposed externally.

## Features Used

* DNS Management
* SSL/TLS Certificates
* Cloudflare Zero Trust

## Initial Setup

The domain was connected to Cloudflare and DNS management was migrated successfully.

After propagation completed, DNS records could be managed through the Cloudflare dashboard.

## Zero Trust

Cloudflare Zero Trust was evaluated as a potential authentication layer for selected services.

During testing, GitHub authentication was configured as an identity provider.

## Challenges Encountered

### GitHub Identity Provider Setup

Configuring GitHub authentication required creating OAuth credentials.

The setup process involved:

* Creating a GitHub OAuth Application
* Generating a Client ID
* Generating a Client Secret
* Configuring callback URLs
* Connecting GitHub to Cloudflare Zero Trust

### Callback URL Discovery

The most confusing part of the setup was locating the correct callback URL required by GitHub.

Without the correct callback URL, authentication requests failed.

After identifying the required URL and configuring the OAuth application correctly, authentication succeeded.

## Current Status

Cloudflare is operational and currently provides:

* DNS management
* SSL/TLS handling
* Zero Trust experimentation

## Lessons Learned

* Cloudflare provides many features, but the interface can be overwhelming for new users.
* OAuth integrations often require careful attention to callback URLs.
* Following high-quality tutorials significantly reduces setup complexity.
* Good documentation is essential because Cloudflare configurations are difficult to remember months later.
