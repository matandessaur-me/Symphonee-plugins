# DevOps Pilot Plugin Registry

Official plugin registry for [DevOps Pilot](https://github.com/matandessaur-me/DevOps-Pilot).

## Available Plugins

| Plugin | Description | Author |
|--------|-------------|--------|
| [Builder.io](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-builderio) | Manage Builder.io models, schemas, and content | M8N-MatanDessaur |
| [Wrike](https://github.com/M8N-MatanDessaur/devops-pilot-plugin-wrike) | Task management, board view, cross-sync with ADO | M8N-MatanDessaur |

## How to Submit a Plugin

1. Create a GitHub repo with your plugin (must have a `plugin.json` at the root)
2. Fork this repo
3. Add your plugin to `registry.json`
4. Submit a pull request

## Plugin Structure

Your plugin repo must contain at minimum:
- `plugin.json` -- manifest with id, name, version, description, contributions
- `routes.js` -- server-side API routes (if needed)

See the [Plugin SDK docs](https://github.com/matandessaur-me/DevOps-Pilot) for full documentation.
