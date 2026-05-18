# stdio-github

Test plugin for evaluating whether Cowork loads a plugin-shipped `.mcp.json` that uses stdio transport against a locally installed `github-mcp-server` binary.

**Setup before installing:**

1. Install the GitHub MCP server binary into `~/.local/bin/github-mcp-server`:

   ```bash
   mkdir -p ~/.local/bin && \
   curl -fL "https://github.com/github/github-mcp-server/releases/latest/download/github-mcp-server_Darwin_$(uname -m).tar.gz" | \
     tar -xz -C ~/.local/bin github-mcp-server
   ```

2. Generate a fine-grained GitHub PAT: <https://github.com/settings/personal-access-tokens/new>
3. Open `.mcp.json` in this plugin directory.
4. Replace `REPLACE_WITH_YOUR_PAT` with the token value.
5. Install this plugin in Cowork and restart.

**Success criterion:** After restart, GitHub MCP tools should be available in Cowork, sourced from this plugin's `.mcp.json` rather than from `claude_desktop_config.json`.
