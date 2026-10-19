# HeyQuad plugin

This plugin lets an AI app work your HeyQuad team inbox as you. It reads and triages your email,
pulls in customer context, writes reply drafts for you to review and send, and files conversations.
**It never sends email.**

Connect it to:
- Claude (Claude Code, Claude.ai, Claude Desktop)
- ChatGPT and Codex
- any MCP client: `https://mcp.heyquad.com/mcp`

## Requirements

- A HeyQuad account.
- Your organization's admin has turned on **Settings › Inbox & email › AI apps (MCP)**.

You sign in with your HeyQuad login and pick one organization. The app can only do what you can do
in HeyQuad yourself, and only in that organization. To revoke access, go to **Account › Connected
apps** in HeyQuad.

## Install

- **Claude Code:**
  ```
  claude plugin marketplace add HeyQuad/heyquad-plugin
  claude plugin install heyquad@heyquad
  ```
  To use the server without the plugin:
  `claude mcp add --transport http heyquad https://mcp.heyquad.com/mcp`
- **Claude.ai / Claude Desktop:** find HeyQuad in the Connectors directory, or add a custom
  connector with `https://mcp.heyquad.com/mcp`.
- **ChatGPT / Codex:** find HeyQuad in the Plugins directory.

## What's in this package

| Path | For |
|---|---|
| `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json`, `.mcp.json` | Claude Code plugin and marketplace |
| `plugin.json`, `mcp.json` | OpenAI plugin (ChatGPT and Codex), portable Agent Plugins format |
| `skills/heyquad-email/SKILL.md` | The workflow both use |
| `assets/` | Icon and logo |

## Privacy

The plugin works with data in your HeyQuad account and sends it to the AI app you connected:
- email messages, threads, internal notes and labels
- contacts and companies
- tickets and deals
- call and voicemail summaries
- knowledge-base passages
- booking availability

It does this only when you or the app ask for it. HeyQuad does not store your conversations with
the AI app. What the AI app does with the data falls under that app's own terms and privacy policy.

HeyQuad's privacy policy: https://heyquad.com/privacy. Terms: https://heyquad.com/terms.
Support: https://heyquad.com/support.
