# Public And Private Boundary

Roadscript is organized to make the application layer reviewable in public while keeping the core Engine private.

## Why The Engine Remains Private

- The Engine contains the core implementation and product-sensitive work.
- Keeping the Engine private protects the core package boundary while the product is still evolving.
- Public repositories can still demonstrate architecture, packaging, and workflow design without publishing the implementation itself.

## What Public Repositories Intentionally Expose

- Repository structure and ownership boundaries
- CMake package consumption at the application layer
- CLI design and workflow examples
- Documentation, tests, examples, and tooling organization
- High-level architecture and development milestones

## What Public Repositories Intentionally Do Not Expose

- Core Engine source code
- Algorithm-specific implementation details
- Internal experiments or sensitive product work
- Local development paths, credentials, or private repository references

## Review Principle

The goal of the public material is to make the project understandable and technically credible without disclosing private implementation detail. That means the public repositories emphasize architecture, packaging, workflow design, and documentation quality rather than core Engine internals.
