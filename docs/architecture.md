# Architecture Overview

The `roadscript-docs` repository documents the public structure around Roadscript without exposing private Engine implementation details.

## High-Level Components

- `roadscript-engine` is the private core package repository.
- `roadscript-cli` is the public application and tooling repository.
- `roadscript-site` is the public-facing website and demo surface repository.
- `roadscript-docs` provides overview material, architecture notes, and repository boundary documentation.

## Package Boundary

The Engine is published internally from `roadscript-engine` as an installable CMake package:

- Package name: `RoadscriptEngine`
- Public CMake target: `Roadscript::rsengine`

The CLI consumes that package through standard CMake dependency boundaries rather than by including Engine source files directly.

## Responsibility Split

### Private Engine

- Owns the portable C++ watermarking core
- Preserves implementation details and core IP
- Exposes a stable package boundary for downstream consumers

### Public CLI

- Owns the standalone command-line application
- Includes the local TUI prototype
- Demonstrates workflow orchestration, docs, examples, tests, and tooling
- Shows how the application layer integrates with the installed Engine package

### Public Site / Demo

- Presents public-facing workflows and product direction
- Can rely on mock data by default so static deployments do not require local backend services

## What This Repo Covers

The `roadscript-docs` repository is intentionally high-level. It focuses on repository organization, ownership boundaries, development milestones, and review-friendly context for collaborators or recruiters.
