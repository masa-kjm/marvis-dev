# marvis-dev

This repository contains reusable skills for development work. See the [marvis-dev plugin README](plugins/marvis-dev/README.md) for its design and file layout.

## Install from Git

The plugin is in `plugins/marvis-dev/`. Each tool installs the same set of skills from this directory. You do not need a setup script or a listing in a public marketplace. The machine must have access to this Git repository.

### Codex

Install:

```sh
codex plugin marketplace add masa-kjm/marvis-dev
codex plugin add marvis-dev@marvis-dev
```

Update:

```sh
codex plugin marketplace upgrade marvis-dev
```

### Claude Code

Install:

```sh
claude plugin marketplace add masa-kjm/marvis-dev
claude plugin install marvis-dev@marvis-dev
```

### GitHub Copilot CLI

Install:

```sh
copilot plugin marketplace add masa-kjm/marvis-dev
copilot plugin install marvis-dev@marvis-dev
```

### Cursor

In Customize → Plugins, add the GitHub repository `masa-kjm/marvis-dev`, then install `marvis-dev`. For a team, import the repository into a Team Marketplace.
