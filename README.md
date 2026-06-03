# OpenClaw — WebRobot plugin

The **WebRobot** ETL platform packaged as an **OpenClaw** plugin: **10 skills**
(invokable as `/` slash commands) plus the hosted **WebRobot MCP** (33 tools) —
pipeline builder, stage catalog, job & dataset management, and the agentic
designer wizard.

This plugin uses the **hosted MCP** at `https://mcp.webrobot.eu/mcp` — no local
process or dependency to install.

## Install (OpenClaw)

Add this repository as a plugin source in OpenClaw and install `openclaw`:

```
/plugin marketplace add https://github.com/WebRobot-Ltd/openclaw-plugin
/plugin install openclaw
```

OpenClaw loads the skills under `/` and connects the `webrobot` MCP server
(HTTP) on demand. Nothing to install locally.

## Skills

`webrobot-overview` · `webrobot-pipeline` · `webrobot-cli` · `webrobot-admin`
· `webrobot-plugin-dev` · `webrobot-frontend-plugin-dev` · `webrobot-python-extension`
· `webrobot-sdk-python` · `webrobot-sdk-java` · `webrobot-sdk-nodejs`

## Layout

```
.claude-plugin/plugin.json   Plugin manifest (name, mcpServers → hosted MCP)
.mcp.json                    Stand-alone MCP entry (other MCP clients)
skills/<name>/SKILL.md       Self-contained skills
```

## Links

- WebRobot: https://webrobot.eu · Portal: https://portal.webrobot.eu
- MCP endpoint: https://mcp.webrobot.eu/mcp (docs: https://portal.webrobot.eu/mcp)

> The plugin layout follows the open `.claude-plugin/plugin.json` + `skills/`
> convention. If the OpenClaw marketplace expects a different manifest, only the
> manifest changes — the `skills/` are format-agnostic markdown.
