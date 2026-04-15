# Symphonee Plugin Registry & Shared Intelligence

Official plugin registry and shared learnings for [Symphonee](https://github.com/matandessaur-me/Symphonee) -- the execution engine for AI workflows.

## What This Repo Contains

- **registry.json** -- Plugin registry listing all available plugins, versions, and repo URLs
- **learnings.json** -- Collective intelligence shared across all Symphonee installations

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [Builder.io](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-builderio) | Manage Builder.io models, schemas, and content | 1.2.0 |
| [Wrike](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-wrike) | Task management, board view, cross-sync with ADO | 1.1.0 |
| [GA4 & GTM](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-ga4-gtm) | Google Analytics 4 and Tag Manager dashboard | 1.1.0 |
| [Dependency Inspector](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-dependency-inspector) | Scan repos for vulnerable and outdated dependencies | 1.1.0 |
| [Release Manager](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-release-manager) | Track ADO pipelines, generate release notes | 1.1.0 |
| [Environment Manager](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-env-manager) | Manage .env files across repos | 1.1.0 |
| [Sentry](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-sentry) | Monitor application errors via Sentry | 1.1.0 |

> Plugin package names still use the `devops-pilot-plugin-*` prefix for install-base stability. A later release will migrate them to `symphonee-plugin-*`.

## Shared Learnings (Collective Intelligence)

Symphonee instances automatically record generic technical learnings (CLI quirks, shell gotchas, platform issues) and can sync them through this repo. This creates a collective knowledge base that makes every installation smarter over time.

**How it works:**
1. When an AI agent encounters a technical failure (wrong CLI flags, shell issues, etc.), the system records it locally.
2. On sync, unsynced learnings are pushed to `learnings.json` in this repo.
3. On startup, every instance pulls the latest shared learnings.
4. Learnings are injected into AI instruction files so agents avoid known pitfalls.

**Safety guarantees:**
- No company names, project names, or client data is ever recorded.
- No secrets, API keys, tokens, or credentials.
- No URLs, file paths, or machine-specific information.
- All content is sanitized before local storage and again before sharing.
- Entries containing sensitive content are automatically rejected.

## How to Submit a Plugin

1. Create a GitHub repo with your plugin (must have a `plugin.json` at the root).
2. Fork this repo.
3. Add your plugin to `registry.json`.
4. Submit a pull request.

## Plugin Structure

Your plugin repo must contain at minimum:
- `plugin.json` -- manifest with id, name, version, description, contributions
- `routes.js` -- server-side API routes (if needed)

See the [Symphonee repo](https://github.com/matandessaur-me/Symphonee) for full SDK documentation.
