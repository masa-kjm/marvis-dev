# Repository Overview

This repository contains reusable components for development harnesses. It currently contains only the marvis-dev plugin, but its scope may expand.

For repository navigation, see the [Codebase Map](../.marvis/codebase/README.md) if it exists.

## Design Principles

- Keep harness components independent of any particular agent platform, including Claude, Codex, and custom agents.
- Favor portable designs that can scale as language models improve, while avoiding overly complex or redundant structures that might hinder such adaptation.

## Documentation Style

- Do not insert line breaks within paragraphs solely to align text.
- Use "ASD-STE100 Simplified Technical English" for any documents or comments to be committed.

## Development

- When making revisions, also update `docs/README.md` as necessary.
