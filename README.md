# EscapeBot for Claude Code and Cowork

Public Claude plugin for [EscapeBot](https://escape-bot.com). It connects Claude Code and Cowork to the hosted research MCP. **This repository contains no EscapeBot application source.** The server runs at `https://api.escape-bot.com/mcp`.

Research only. EscapeBot does not place trades.

## Supported surfaces

| Surface | Supported | How |
| --- | --- | --- |
| Claude Code | Yes | This plugin |
| Cowork | Yes | This plugin |
| Claude Chat | Use the same MCP URL as a custom connector, or the Connectors Directory listing once published |

The plugin and the remote connector talk to the same hosted MCP. The connector is the raw tools; this plugin adds research skills and slash commands on top.

## Install

### Claude Code

This repository is its own plugin marketplace:

```shell
/plugin marketplace add asheinking/escapebot-claude-plugin
/plugin install escapebot@escapebot
```

To try it without installing, clone the repository and run:

```shell
claude --plugin-dir ./escapebot-claude-plugin
```

### Cowork

Open Customize → Plugins, select Add marketplace, enter `https://github.com/asheinking/escapebot-claude-plugin`, then install **EscapeBot**. Cowork prompts you to sign in during install.

## Auth

Sign in with an existing EscapeBot account when Claude opens Connect (OAuth). Billing stays on escape-bot.com. The plugin does not collect payment. Details: [SETUP.md](SETUP.md).

## Skills and commands

| Name | What it does |
| --- | --- |
| `escapebot` skill | How Claude should call the forecast, valuation, quotes, news, screener, and filings |
| `/escapebot:forecast` | Custom forecast and what drives it for a ticker |
| `/escapebot:fair-value` | EscapeBot fair value for a ticker |
| `/escapebot:screen` | Equity screen via `get_screener_filter_specs` then `run_screen` |

Example prompts:

- What is the custom forecast for NVDA and what factors support it?
- What is EscapeBot's fair value estimate for AAPL?
- Screen profitable large-cap stocks using forecast and valuation metrics
- What are the latest news stories for NVDA?

## What is in this repo

| Path | Purpose |
| --- | --- |
| `.claude-plugin/plugin.json` | Plugin manifest |
| `.claude-plugin/marketplace.json` | Direct-install marketplace catalog |
| `.mcp.json` | Hosted MCP URL |
| `skills/escapebot/SKILL.md` | How the agent should use EscapeBot tools |
| `commands/` | Slash commands |
| `SETUP.md` | OAuth sign-in |
| `assets/logo.png` | Plugin logo (same mark as escape-bot.com) |

## Legal

- Privacy: https://escape-bot.com/privacy-policy
- Terms: https://escape-bot.com/terms-of-service
- Support: support@escape-bot.com
- License: [MIT](LICENSE)
