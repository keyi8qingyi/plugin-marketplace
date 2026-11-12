---
name: frontend-design-setup
description: Guide installation of Anthropic's Frontend Design plugin for Claude Code.
---

# Frontend Design Setup

Explain the setup by default. Install or configure the upstream plugin only when the user requests installation in a specific client and environment. Check for an existing installation and use the client's native configuration or package cache. Keep upstream files, dependencies, and credentials out of this market checkout.

Use when the user asks to set up Anthropic's Frontend Design plugin for web UI work.

- In Claude Code, use `/plugin install frontend-design@claude-plugins-official`. Check `claude plugin list` for the exact upstream plugin ID.
- Start a new Claude Code session and confirm the Frontend Design skill is available. A suitable test is to ask for design feedback on a sample settings page while keeping the task read-only.
- For another client, check whether Anthropic documents a supported distribution route for that client before proposing installation.

[Anthropic Frontend Design](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/frontend-design)
