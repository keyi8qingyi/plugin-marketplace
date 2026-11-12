---
name: openai-developers-setup
description: Guide installation of the official OpenAI Developers plugin for API and SDK work.
---

# OpenAI Developers Setup

Explain the setup by default. Install or configure the upstream plugin only when the user requests installation in a specific client and environment. Check for an existing installation and use the client's native configuration or package cache. Keep upstream files, dependencies, and credentials out of this market checkout.

Use when the user asks to set up the official OpenAI Developers plugin.

- In Codex CLI, open `/plugins`, search for OpenAI Developers, and select the official listing. In the desktop app, use the Plugins directory. Follow the client's setup prompts if the user wants the OpenAI Platform connection.
- In Claude Code, use `/plugin marketplace add openai/openai-developers-for-claude` if that source is missing, then `/plugin install openai-developers@openai-developers`.
- Start a new session. Confirm installation in the target client's plugin inventory and ask a documentation question about the Responses API. Account connection and project API keys are separate steps that require the user's intended account and project.

[Official OpenAI installation guide](https://developers.openai.com/learn/developers-codex-plugin)
