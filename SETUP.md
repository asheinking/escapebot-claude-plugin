# EscapeBot setup

The plugin connects Claude to EscapeBot's hosted MCP at `https://api.escape-bot.com/mcp`. Authentication is OAuth. This repository ships no credentials, tokens, or headers.

## What you need

- An existing EscapeBot account. Billing stays on [escape-bot.com](https://escape-bot.com). This plugin does not collect payment.
- Claude Code, or Cowork with plugin support.

Claude Chat / claude.ai users add the same server as a custom connector (or, once listed, from the Connectors Directory). That is a separate listing from this plugin.

## Claude Code

1. Install the plugin (see [README](README.md#install)).
2. Run `/mcp`, select **escapebot**, and authenticate. Claude Code opens EscapeBot sign-in in the browser.
3. Sign in with your EscapeBot account and approve access.

## Cowork

1. Install the plugin from Customize → Plugins (see [README](README.md#install)).
2. When the connector needs authentication, complete EscapeBot OAuth during install.
3. Manage the connector from the installed plugin's connector page.

## Confirm it works

Ask Claude: "What is the Oracle score for NVDA and why?" It should call EscapeBot tools rather than invent a score.

## Reconnect or disconnect

- Claude Code: `/mcp` → **escapebot** → re-authenticate or clear authentication.
- Cowork: sign out or back in from the plugin's connector page.
- Uninstalling the plugin removes the connector from that surface only. It does not change your EscapeBot account.
