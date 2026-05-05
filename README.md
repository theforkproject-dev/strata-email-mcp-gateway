# Strata Email MCP Gateway

Public Tinfoil config repo for the Strata Email MCP gateway POC.

This config exposes a Claude-compatible MCP endpoint that projects the verified email action surface and routes Level 1 mechanical witness requests to the live official Tinfoil witness.

The gateway image/source may remain private. This repo is the public measurement/config surface:

- pinned image digest
- Tinfoil resource config
- exposed HTTP paths
- public registry/policy/witness URLs
- non-secret runtime settings
- Tinfoil secret names, not secret values

The first deployment uses `EMAIL_PROVIDER=dry-run` so it proves the MCP/gateway/witness/certificate path without sending real email.
