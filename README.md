# atlas-cartograph

Cartograph is a GitHub Copilot canvas for exploring, searching, and chatting with one or more Atlas knowledge stores.

![Cartograph galaxy overview](docs/images/hero-galaxy.png)

![Cartograph graph with chat and knowledge activation](docs/images/hero-activity.png)

![Cartograph page preview](docs/images/hero-preview.png)

## Why / what this is not

Cartograph makes Atlas content and relationships visible and navigable. Its layout organizes a graph visually; it does not invent relationships. Atlas mounts are data, not executable code.

## Capabilities

- View one or more Atlas stores as a galaxy of connected pages.
- Search pages across open stores, follow schema layers, and preview content.
- Chat with the mounted knowledge and see live graph updates and file-access activity.

## Install

Enable the canvas feature, then add the catalog and install the package:

```bash
apm experimental enable canvas
apm marketplace add sergio-sisternes-epam/atlas-marketplace --name atlas
apm install atlas-cartograph@atlas
```

Canvas packages execute code. Before installing, grant only the canvas capability in the consuming project's `apm.yml`:

```yaml
executables:
  allow:
    sergio-sisternes-epam/atlas-cartograph:
      canvas: true
```

See [canvas approval](docs/usage.md#canvas-approval) for offline archives and the exact approval key.

## Use

1. Reload project extensions, then open **+ → Canvas → Cartograph** and choose `project:cartograph` if both project and user extensions are listed.
2. With no explicit root, Cartograph opens recognized Atlas stores under the current project's `.atlas/`; if none are found, choose a store from the picker.
3. Use the map to search, follow layers, preview pages, and chat with the mounted knowledge.

![Open Cartograph from the Canvas menu](docs/images/use-open-canvas.png)

For source checkouts, Node.js 22 or later is required; run `npm start` without an npm install or build. See [usage](docs/usage.md), [access monitoring](docs/file-access.md), and [architecture](docs/architecture.md) for details.

## Prerequisites

Use the GitHub Copilot App and APM CLI with canvas support enabled. Running Cartograph from a source checkout additionally requires Node.js 22 or later.

## Related

- [Atlas marketplace](https://github.com/sergio-sisternes-epam/atlas-marketplace) — package catalog.
- [`atlas`](https://github.com/sergio-sisternes-epam/atlas) — knowledge package required by this canvas.
- [Usage guide](docs/usage.md) — operation and canvas approval details.

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Report vulnerabilities through a [private GitHub security advisory](https://github.com/sergio-sisternes-epam/atlas-cartograph/security/advisories/new), not a public issue.

## License

Copyright 2026 Sergio Sisternes. Licensed under the [Apache License 2.0](LICENSE).
