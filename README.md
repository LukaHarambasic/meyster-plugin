# Meyster plugin for Claude and ChatGPT

Meyster is business software for German trade and construction businesses. This plugin connects Claude or ChatGPT to your Meyster account. Claude can find customers, calculate quantities, and draft quotes (Angebote) and invoices (Rechnungen) for you. Every draft comes with a link. You check it and finish it in Meyster.

## What it includes

- The remote MCP server `meyster` at `https://meyster.work/mcp` (OAuth sign in, no key to paste).
- Skills: `einrichten` (setup, the onboarding skill in ChatGPT) and `meyster`, which tells the app to load the matching Meyster skill with `load_skill` before each task. The rules themselves come from the Meyster server, so they are the same rules Meyster's own assistant follows, plus the company's own description and rules.
- Commands for Claude Code: `/meyster:angebot` and `/meyster:rechnung`.

## What it never does

Claude creates drafts only. It never finalizes, numbers, sends or cancels a document, and it never deletes a customer. Those steps stay with a person in Meyster. Document texts are written in the company's language, and legal notes stay German.

## Requirements

- A Meyster account at https://meyster.work.
- The owner of your company has switched on "KI-Apps verbinden (MCP)" in the company settings. While it is off, the connection is refused.

## Install

In Claude Code:

```
/plugin marketplace add LukaHarambasic/meyster-plugin
/plugin install meyster@meyster-plugins
```

When the plugin is listed in the Claude Directory, add it from there instead. On first use Claude opens a Meyster page where you sign in and approve the connection. You can disconnect the app at any time in the Meyster company settings.

## Two formats in one folder

| File | Read by |
|---|---|
| `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json`, `.mcp.json`, `commands/` | Claude |
| `plugin.json`, `mcp.json` | ChatGPT and Codex (Agent Plugins format) |
| `skills/`, `assets/` | both |

The ChatGPT package is a ZIP of the portable files only:

```
zip -r meyster-openai.zip plugin.json mcp.json skills assets
```

Upload it at https://platform.openai.com/plugins. Raise `version` in both manifests for every release.

## Data and privacy

Claude reads and writes the records of your own company through your own Meyster rights. Nothing else is sent anywhere by this plugin. Privacy policy: https://meyster.work/datenschutz

## Support

luka@meyster.work
