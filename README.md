# marvis-dev

This repository contains reusable skills for development work. See [docs/README.md](docs/README.md) for the design and file layout.

## Install from Git

The plugin is in `plugins/marvis-dev/`. Each tool installs the same set of skills from this directory. You do not need a setup script or a listing in a public marketplace. The machine must have access to this Git repository.

| Tool | Installation |
| --- | --- |
| Codex | Run `codex plugin marketplace add masa-kjm/marvis-dev`, then `codex plugin add marvis-dev@marvis-dev`. |
| Claude Code | Run `claude plugin marketplace add masa-kjm/marvis-dev`, then `claude plugin install marvis-dev@marvis-dev`. |
| GitHub Copilot CLI | Run `copilot plugin marketplace add masa-kjm/marvis-dev`, then `copilot plugin install marvis-dev@marvis-dev`. |
| Cursor | In Customize → Plugins, add the GitHub repository `masa-kjm/marvis-dev`, then install `marvis-dev`. For a team, import the repository into a Team Marketplace. |
