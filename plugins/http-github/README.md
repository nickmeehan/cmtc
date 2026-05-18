# http-github

Test plugin for evaluating whether Cowork loads a plugin-shipped `.mcp.json` that uses HTTP transport against GitHub's hosted MCP endpoint (`https://api.githubcopilot.com/mcp`).

**Setup before installing:**

1. Generate a fine-grained GitHub PAT: <https://github.com/settings/personal-access-tokens/new>
2. Open `.mcp.json` in this plugin directory.
3. Replace `REPLACE_WITH_YOUR_PAT` with the token value.
4. Install this plugin in Cowork and restart.

**Success criterion:** After restart, GitHub MCP tools should be available in Cowork, sourced from this plugin's `.mcp.json` rather than from `claude_desktop_config.json`.
