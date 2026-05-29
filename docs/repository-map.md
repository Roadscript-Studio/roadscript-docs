# Repository Map

This document summarizes which Roadscript repositories are public, which remain private, and what each one owns.

| Repository | Visibility | Owns | Notes |
| --- | --- | --- | --- |
| `roadscript-docs` | Public | Overview docs, architecture notes, repository boundaries, milestone summaries | Intended as the public company/project documentation entry point |
| `cyphra-cli` | Public | CLI, workflow DSL, local TUI prototype, examples, tests, and tools | Public repository for Cyphra CLI, the developer-facing command-line and workflow layer |
| `roadscript-engine` | Private | Portable C++ core watermarking package | Exported as `RoadscriptEngine` with public target `Roadscript::rsengine` |
| `roadscript-site` | Public / public-facing | Website and demo surface | Can default to mock data for static deployments |

## Public Repositories

The public repositories are intended to show:

- application architecture
- Cyphra CLI and workflow structure
- examples, tests, and tooling
- documentation quality and repository discipline

## Private Repository

The private `roadscript-engine` repository exists to protect the core implementation boundary while still allowing `cyphra-cli` to demonstrate real integration through CMake package consumption.
