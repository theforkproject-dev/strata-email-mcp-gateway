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

The current deployment uses `EMAIL_PROVIDER=resend` and OAuth so Claude Desktop and other Anthropic MCP clients can authorize with PKCE, call the remote `/mcp` endpoint, and send real verified email through the witnessed gateway.

OAuth state is stored at `/mnt/ramdisk/email-mcp/oauth-store.json` for the demo. Client registrations and refresh tokens survive while the container is running, but are lost on relaunch.
