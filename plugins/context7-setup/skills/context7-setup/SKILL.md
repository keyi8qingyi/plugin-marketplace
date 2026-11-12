---
name: context7-setup
description: Guide installation of Upstash Context7 for version-specific library documentation.
---

# Context7 Setup

Explain the setup by default. Install or configure the upstream plugin only when the user requests installation in a specific client and environment. Check for an existing installation and use the client's native configuration or package cache. Keep upstream files, dependencies, and credentials out of this market checkout.

Use when the user asks to set up Context7 or wants a client-specific installation plan.

- In Claude Code, install `context7@claude-plugins-official` with `/plugin install context7@claude-plugins-official`. The upstream plugin connects to the hosted MCP service.
- For another MCP client, use [Context7's client setup guide](https://context7.com/docs/resources/all-clients) and the hosted endpoint `https://mcp.context7.com/mcp`. Follow the provider's current authentication instructions. Keep any API key in the target client's secret configuration.
- Start a new session and ask Context7 for documentation for a named public library at a specific version. Confirm the lookup used Context7.

[Upstream repository](https://github.com/upstash/context7) · [Claude Code marketplace](https://github.com/anthropics/claude-plugins-official/blob/main/.claude-plugin/marketplace.json)
