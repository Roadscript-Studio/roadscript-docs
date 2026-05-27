# Roadscript

Roadscript is an authenticity tooling project focused on application workflows around invisible watermarking and media provenance.

## Project Status

Roadscript is in active development. Public repositories are application- and documentation-focused, while the core Engine remains private as productization continues.

## Repository Map

| Repository | Visibility | Purpose |
| --- | --- | --- |
| `roadscript-cli` | Public | Standalone CLI, workflow DSL, local TUI prototype, docs, examples, tests, and tooling |
| `roadscript-engine` | Private | Portable C++ core package exported as an installable CMake package |
| `roadscript-docs` | Public | Project overview, architecture notes, repository boundaries, and development milestones |
| `roadscript-site` | Public / public-facing | Website and demo surface that can use mock data for static deployment |

## Architecture Overview

- The private `roadscript-engine` repository contains the core C++ package and implementation boundary.
- The public `roadscript-cli` repository consumes the Engine through a CMake package boundary.
- The package boundary is `RoadscriptEngine`, with the public target `Roadscript::rsengine`.
- `roadscript-site` provides the public-facing website and demo surface and can default to mock data when deployed statically.
- The public `roadscript-docs` repository explains the overall structure, development direction, and public/private boundaries.

## What Is Public

- CLI and application-layer architecture
- Workflow DSL examples and usage patterns
- Documentation and repository split notes
- High-level system organization
- Test, example, and tooling structure in `roadscript-cli`

## What Remains Private

- Core Engine source code
- Implementation internals and algorithm-specific details
- Product-sensitive experiments and engine-side research

## Recent Milestone

Roadscript recently moved from a monorepo-style setup into clearer repository boundaries:

- `roadscript-engine` was separated into a private, installable C++ package.
- `roadscript-cli` became a standalone public application repository.
- The CLI now consumes the installed Engine package instead of bundling Engine source directly.
- The package boundary is exposed as `RoadscriptEngine` / `Roadscript::rsengine`.
- Public-facing materials were sanitized to remove local paths, private source references, and internal implementation detail.

## For Reviewers And Recruiters

This repository is meant to make the Roadscript project legible at a glance: what exists, what is public, what remains private, and what the public repositories demonstrate technically.

Roadscript demonstrates:

- C++ package architecture with a clean export/consume boundary
- CMake package installation and downstream linking
- CLI and workflow design
- Repository separation between public application layers and private core IP
- Documentation discipline around public-safe technical communication
- Organized examples, tests, and tooling in `roadscript-cli`

## Additional Docs

- [Architecture Overview](docs/architecture.md)
- [Repository Map](docs/repository-map.md)
- [Development Log](docs/development-log.md)
- [Public / Private Boundary](docs/public-private-boundary.md)

## Links

- `roadscript-cli`: [github.com/Roadscript-Studio/roadscript-cli](https://github.com/Roadscript-Studio/roadscript-cli)
- `roadscript-site`: [github.com/Roadscript-Studio/roadscript-site](https://github.com/Roadscript-Studio/roadscript-site)
- `roadscript-docs`: [github.com/Roadscript-Studio/roadscript-docs](https://github.com/Roadscript-Studio/roadscript-docs)
- `roadscript-engine`: private repository, not publicly linked

## License

License information will be added before external reuse. Public content is provided for portfolio and project review.
