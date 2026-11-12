# Baton Market

Baton Market is a Git repository of self-contained agent plugins. Clone the repository to browse the plugins, or use the repository as a native marketplace in a supported client.

## Plugins

| Plugin | What it does |
| --- | --- |
| [Diff Review](plugins/review-diff/) | Reviews Git changes for bugs, regressions, and gaps in verification. |
| [Bug Investigation](plugins/trace-bug/) | Tests competing hypotheses to narrow down the cause of a failure. |
| [Release Notes](plugins/draft-release-notes/) | Drafts release notes with user impact and required upgrade steps. |

## Upstream plugin setup guides

These entries contain setup skills. Open a guide or install its `-setup` entry to let an agent explain the upstream installation. When asked to install the upstream plugin, the agent should use the selected client's normal installation location outside this checkout.

| Guide | Use it for |
| --- | --- |
| [Context7 Setup](plugins/context7-setup/skills/context7-setup/SKILL.md) | Library documentation and examples for a specific version. |
| [Playwright MCP Setup](plugins/playwright-setup/skills/playwright-setup/SKILL.md) | Browser automation and UI smoke tests. |
| [Frontend Design Setup](plugins/frontend-design-setup/skills/frontend-design-setup/SKILL.md) | Anthropic's frontend design skill for Claude Code. |
| [OpenAI Developers Setup](plugins/openai-developers-setup/skills/openai-developers-setup/SKILL.md) | OpenAI API and SDK workflows in supported clients. |
| [LayerFS Setup](plugins/layerfs-setup/skills/layerfs-setup/SKILL.md) | Reuse a LayerFS image, build one from source, or connect through the SDK. |

## Plugin layout

Each plugin lives at `plugins/<id>/`. Its directory name matches the `name` in its manifest. A host that discovers plugins under `${DataDir}/plugins/` can copy the whole directory to `${DataDir}/plugins/<id>/`.

```text
plugins/<id>/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── <skill-name>/
│       └── SKILL.md
├── .codex-plugin/
│   └── plugin.json
├── gemini-extension.json
└── plugin.json
```

The manifest at `.claude-plugin/plugin.json` carries the plugin ID, display name, version, and description. Add `userConfig` when the plugin needs host-provided settings. Add `.mcp.json` for an MCP-backed plugin, `references/` inside a skill for supporting material, and `ui/` when a plugin ships an MCP App view. The current plugins contain skills and require no settings.

Client-specific manifests are included for supported targets. Setup guides include Claude Code and Codex manifests. Keep the metadata consistent across manifests and update the relevant root marketplace indexes when adding or removing a plugin.

## Install from a checkout

Run the commands for your client from the repository root. These examples install Diff Review.

**Codex**

```sh
codex plugin marketplace add "$PWD"
codex plugin add review-diff@baton-market
```

**Claude Code**

```sh
claude plugin marketplace add "$PWD"
claude plugin install review-diff@baton-market
```

**Gemini CLI**

```sh
gemini extensions install "$PWD/plugins/review-diff"
```
