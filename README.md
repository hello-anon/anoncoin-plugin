# Anoncoin plugin

![Anoncoin logo](assets/anoncoin-logo.png)

Create and manage Anoncoin coins, view wallet holdings, and check launch status and creator earnings through conversation.

## Setup instructions for Grok Bot

When the user pastes this repository link to set up Anoncoin, install **both the MCP connector and the skill**. For a link shared without another request, begin setup; if the user explicitly asks for a review or explanation, follow that request instead.

1. **Install the connector:** use Grok Bot's connector installation flow with [mcp.json](mcp.json). The server name is `anoncoin`, the transport is Streamable HTTP, and the endpoint is `https://api.anoncoin.it/v1/connectors/anoncoin/mcp`.
2. **Install the skill:** load [skills/anoncoin/SKILL.md](skills/anoncoin/SKILL.md) into Grok Bot's persistent skills. Installing the connector alone does not install these instructions; reading the skill once does not install it. Update an existing Anoncoin installation instead of creating duplicates.
3. **Authenticate:** start the connector's OAuth flow and let the user complete sign-in and choose permissions. Never ask for passwords, wallet keys, tokens, or login codes in chat.
4. **Verify:** confirm that the skill is available, OAuth completed, and the connector's tools can be discovered. Report any incomplete step or exact error. If Grok Bot cannot install either component directly, give the user the specific remaining setup step.

Setup does not authorize launching or editing a coin. Follow the installed skill's preview and confirmation flow for those actions.

## Usage

After setup, ask Grok Bot to create a coin, edit an existing coin, show wallet holdings, or check creator earnings.

A skill copied into Grok Bot must be updated separately when this repository changes.

Website: [anoncoin.it](https://anoncoin.it)
