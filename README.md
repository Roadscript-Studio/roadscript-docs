# Roadscript

Roadscript is an authenticity tooling project focused on media provenance, invisible watermarking workflows, and verification-oriented application infrastructure.

This repository, `roadscript-docs`, is the public overview and architecture documentation layer for the Roadscript ecosystem. It explains how the repositories fit together, what is public, what remains private, and what the current development milestones demonstrate.

## Project Status

Roadscript is in active development.

The public repositories focus on documentation, application-layer tooling, and the public website/demo surface. The core engine implementation remains private while productization continues.

## Repository Map

| Repository | Visibility | Purpose |
|---|---:|---|
| [`roadscript-docs`](https://github.com/Roadscript-Studio/roadscript-docs) | Public | Public overview, architecture notes, repository boundaries, and development milestones. |
| [`roadscript-cli`](https://github.com/Roadscript-Studio/roadscript-cli) | Public | Standalone CLI, workflow DSL, local TUI prototype, docs, examples, tests, and tooling. |
| [`roadscript-site`](https://github.com/Roadscript-Studio/roadscript-site) | Public | Public website and sample-driven demo surface. |
| `roadscript-engine` | Private | Portable C++ core package exported as an installable CMake package. |

## Architecture Overview

Roadscript is organized around a clear public/private boundary.

- `roadscript-engine` is the private C++ core package and implementation boundary.
- `roadscript-cli` is the public application/tooling layer that consumes the Engine through an installed CMake package.
- The package boundary is `RoadscriptEngine`, with the exported CMake target `Roadscript::rsengine`.
- `roadscript-site` is the public-facing website and demo surface. It can use mock data for static deployment.
- `roadscript-docs` explains the project structure, repository responsibilities, development milestones, and public/private boundaries.

This split allows the public repositories to demonstrate architecture, tooling, documentation, and application-layer engineering while keeping the core Engine implementation private.

## What Is Public

The public Roadscript repositories intentionally expose:

- repository structure and architecture notes
- CLI and application-layer design
- workflow DSL examples and usage patterns
- documentation and repository split history
- website/demo presentation layer
- tests, examples, and tooling structure in `roadscript-cli`

## What Remains Private

The private Roadscript repositories intentionally protect:

- core Engine source code
- implementation internals and algorithm-specific details
- product-sensitive experiments
- engine-side research and integration work

The private Engine is referenced publicly only as a package boundary: `RoadscriptEngine` / `Roadscript::rsengine`.

## Recent Milestone

Roadscript recently moved from a monorepo-style development structure into clearer repository boundaries.

Completed milestones include:

- `roadscript-engine` was separated into a private, installable C++ package.
- `roadscript-cli` became a standalone public application repository.
- `roadscript-cli` now consumes the installed Engine package instead of bundling Engine source directly.
- The CMake package boundary is exposed as `RoadscriptEngine` / `Roadscript::rsengine`.
- `roadscript-site` was renamed and positioned as the public website/demo surface.
- `roadscript-docs` was converted from an internal planning workspace into a public overview and architecture repository.
- Public-facing materials were sanitized to remove local paths, private source references, and implementation-level details.

## For Reviewers And Recruiters

This repository is designed to make Roadscript legible at a glance: what exists, what is public, what remains private, and what the public repositories demonstrate technically.

The Roadscript ecosystem demonstrates:

- C++ package architecture with a clean export/consume boundary
- CMake package installation and downstream linking
- CLI and workflow design
- repository separation between public application layers and private core IP
- documentation discipline around public-safe technical communication
- organized examples, tests, and tooling in `roadscript-cli`
- product-facing presentation through `roadscript-site`

Start here if you want to understand the project structure before looking at the public code repositories.

## Additional Docs

- [Architecture Overview](docs/architecture.md)
- [Repository Map](docs/repository-map.md)
- [Development Log](docs/development-log.md)
- [Public / Private Boundary](docs/public-private-boundary.md)

## Related Repositories

- [`roadscript-docs`](https://github.com/Roadscript-Studio/roadscript-docs) — public overview, architecture notes, and repository boundaries.
- [`roadscript-cli`](https://github.com/Roadscript-Studio/roadscript-cli) — standalone CLI, workflow DSL, local TUI prototype, examples, tests, and tooling.
- [`roadscript-site`](https://github.com/Roadscript-Studio/roadscript-site) — public website and sample-driven demo surface.
- `roadscript-engine` — private C++ core package, not publicly linked.

## License

License information will be added before external reuse. Public content is provided for portfolio and project review.
