# Cloudflare Access GitHub Policy

## Overview

While reviewing the security configuration of the Proxmox web interface, it was discovered that Cloudflare Access was configured to allow any authenticated GitHub user.

The initial assumption was that only the repository owner would be able to pass the Cloudflare Access login screen. A verification test using a secondary GitHub account showed that any valid GitHub account could successfully authenticate.

## Initial Configuration

The Cloudflare Access policy used the following rule:

```text
Include
→ Login Methods
→ GitHub
```

This configuration allows any user with a valid GitHub account to pass the Cloudflare Access authentication layer.

## Security Concern

Although Proxmox authentication was still required after passing Cloudflare Access, the administrative login page was unnecessarily exposed to all authenticated GitHub users.

The goal was to restrict access to authorized identities only.

## Solution

The policy was modified to allow only the primary email address associated with the homelab administrator.

Updated policy:

```text
Include
→ Emails
→ <authorized email address>
```

GitHub remains the identity provider used for authentication.

## Verification

A second GitHub account was used to test the updated policy.

Results:

* Primary GitHub account: Access granted
* Secondary GitHub account: Access denied

The test confirmed that only the intended account can pass the Cloudflare Access authentication layer.

## Lessons Learned

Cloudflare Access identity providers and access policies are separate concepts.

Using GitHub as an identity provider does not automatically restrict access to a specific GitHub account.

Always verify access policies with a secondary account to ensure that only intended users can access administrative services.
