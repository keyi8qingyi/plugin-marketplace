---
name: layerfs-setup
description: Find and use LayerFS in the current environment through an existing image, a source build, or the JavaScript SDK.
---

# LayerFS Setup

Use this skill when the user asks to set up or use LayerFS. Inspect the current environment and choose a route that fits the requested work.

## Inspect the environment

1. Check the operating system, CPU architecture, and available runtime. Look for an existing LayerFS client, MCP entry, SDK, or source checkout. Check the project and any user-provided source paths before looking elsewhere.
2. If Docker is available, list images in the Docker context the Agent will use. Inspect any candidate LayerFS image for its tag, architecture, and intended role. Check the configuration for the target project and Store.
3. Use an existing working integration when it supports the task. A Docker image may provide the workspace runtime without providing an MCP entry point. Verify the image's purpose before using it.

## Choose a setup route

- **Existing image.** Reuse a compatible image and its documented client or runtime configuration. If the deployment provides an MCP configuration, inspect it and preserve its command, arguments, and Store settings when adding the entry to the target client.
- **Source build.** Use an existing LayerFS checkout if it contains the required build files. If the source is missing, start with the [official LayerFS documentation](https://layerfs.ai/docs/) and obtain the source from the [official LayerFS repository](https://github.com/Ephemeral-AI-Lab/layerfs). Use a release or revision compatible with the task and follow that revision's [build guide](https://github.com/Ephemeral-AI-Lab/layerfs/blob/main/api/README.md). Build the image that the integration requires for the current architecture.
- **SDK or CLI.** For direct integration in a script, use the [official SDK reference](https://layerfs.ai/docs/sdk/) to set up `@layerfs/agent` from the LayerFS checkout. For shell-driven work, follow the same revision's CLI setup. Check whether the selected operation needs a native binding, a platform worker, or a Docker runtime. Verify the platform and Store filesystem against the [platform requirements](https://layerfs.ai/docs/platform/).

When setup is requested, carry out the compatible route in the target environment. Use a separate checkout or the target project's normal dependency location for any source or dependencies you obtain. Keep source, image archives, and deployment credentials outside the plugin market. If a prerequisite cannot be met, report the specific failure and try another supported route when it fits the task.

## Verify the integration

Run a read-only LayerFS project, Store, or branch query through the selected interface and confirm the expected result. For build work, resolve the intended branch and workspace path before running commands. Report the route used, the image tag or source revision when applicable, and the result of the check.
