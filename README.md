# Anoncoin plugin

![Anoncoin logo](assets/anoncoin-logo.png)

Production Anoncoin MCP connector and skill for conversational coin creation, coin editing, wallet holdings, launch status, and creator earnings.

## Connection

- Website: https://anoncoin.it
- MCP: https://api.anoncoin.it/v1/connectors/anoncoin/mcp
- Authentication: Anoncoin OAuth using the existing X/Privy sign-in and user-selected permissions. No API keys or wallet keys are bundled.

## Package

- `plugin.json`: portable Agent Plugins manifest.
- `.cursor-plugin/plugin.json`: Cursor manifest with the Anoncoin logo.
- `mcp.json`: remote Streamable HTTP connector configuration.
- `skills/anoncoin/SKILL.md`: Anoncoin conversation and confirmation instructions.
- `assets/anoncoin-logo.png`: Anoncoin logo.

## Flow

Develop the concept, artwork, name, available ticker and description first. Choose an enabled quote token before the final preview. Launch only after explicit approval of the exact preview. After confirmed creation, offer eligible followed-by accounts, another username, and skip using the host's native choice card when available. Selecting an account only prepares an edit preview; saving requires separate confirmation.

## Installation and release checks

Keep this repository private until production verification is complete. Import it with a host that supports the plugin format and private repository access. Verify that both the skill and connector are installed, then authenticate and select permissions. A private skill copied into Grok Bot must be updated separately; repository pushes do not update that copy automatically.

Packaging does not guarantee marketplace acceptance or bundled installation in every host. Check the actual target account and build. No production launch is needed to verify installation.

Before release, verify MCP OAuth discovery, sign-in, selected-scope enforcement, read-only tools, logo rendering and the updated skill. Production launches and edits require their own explicit confirmations.

On 14 October 2026, the configured production MCP endpoint and its protected-resource discovery URL returned HTTP 404. The package is prepared for production, but live production connectivity is not yet verified. Deploy and enable the connector before installation testing.
