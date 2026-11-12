---
name: playwright-setup
description: Guide installation of Microsoft's Playwright MCP server for browser testing.
---

# Playwright MCP Setup

Explain the setup by default. Install or configure the upstream plugin only when the user requests installation in a specific client and environment. Check for an existing installation and use the client's native configuration or package cache. Keep upstream files, dependencies, and credentials out of this market checkout.

Use when the user asks to set up Playwright MCP for UI testing or browser automation.

- In Claude Code, use `/plugin install playwright@claude-plugins-official`.
- In Codex, use `codex mcp add playwright -- npx @playwright/mcp@latest` from the target environment. For other MCP clients, use the matching configuration in Microsoft's README. Choose one setup route per client.
- If using the local MCP server, check Node.js and npm requirements on the target. The package runner can fetch the server, and the target may also need a supported browser. Follow the upstream setup instructions for that runtime.
- Start a new session and verify the browser tools against a local test page or a public example page. Confirm that the target client can return a page title or snapshot.

[Microsoft Playwright MCP](https://github.com/microsoft/playwright-mcp) · [Claude Code marketplace](https://github.com/anthropics/claude-plugins-official/blob/main/.claude-plugin/marketplace.json)
