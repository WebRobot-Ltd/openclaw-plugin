# OpenClaw — WebRobot plugin

The **WebRobot** ETL platform packaged as an OpenClaw / Claude Code plugin:
**10 skills** (invokable as `/` slash commands) plus the hosted **WebRobot MCP**
(33 tools) — pipeline builder, stage catalog, job & dataset management, and the
agentic designer wizard.

Unlike the local-MCP variant, this plugin uses the **hosted MCP** at
`https://mcp.webrobot.eu/mcp` — no local Python process or dependency.

## Install (Claude Code)

```
/plugin marketplace add https://github.com/WebRobot-Ltd/openclaw-plugin
/plugin install openclaw
```

Claude Code loads the skills under `/` and connects the `webrobot` MCP server
(HTTP) on demand. Nothing to install locally.

## Skills

`webrobot-overview` · `webrobot-pipeline` · `webrobot-cli` · `webrobot-admin`
· `webrobot-plugin-dev` · `webrobot-frontend-plugin-dev` · `webrobot-python-extension`
· `webrobot-sdk-python` · `webrobot-sdk-java` · `webrobot-sdk-nodejs`

## Layout

```
.claude-plugin/plugin.json   Plugin manifest (name, mcpServers → hosted MCP)
.mcp.json                    Stand-alone MCP entry (local dev / other clients)
skills/<name>/SKILL.md       Self-contained skills
```

## Links

- WebRobot: https://webrobot.eu · Portal: https://portal.webrobot.eu
- MCP endpoint: https://mcp.webrobot.eu/mcp (see https://portal.webrobot.eu/mcp)
- Claude Code plugin (local MCP variant): https://github.com/WebRobot-Ltd/webrobot-claude-plugin

> NOTE: this follows the Claude Code plugin format (`.claude-plugin/plugin.json`
> + `skills/`). If the OpenClaw marketplace expects a different manifest, adjust
> the manifest only — the `skills/` are format-agnostic markdown.
