# Development Log

This log captures the recent repository and packaging changes that shape the current public Roadscript structure.

## Recent Milestones

1. The original monorepo-style system was split into separate repositories.
2. `roadscript-engine` was converted into an installable C++ package.
3. `roadscript-cli` was initialized as a standalone application repository.
4. The CLI was updated to build against the installed Engine package instead of directly including Engine source files.
5. The Engine stopped owning `apps/cli` and `apps/tui`.
6. The Engine became core-only and remained private.
7. The CLI became application- and tooling-focused and was prepared for public release.
8. The CLI public release was sanitized to remove local paths, sensitive data, private source references, and build artifacts.
9. Public examples were retained in the CLI, including:
   - `examples/classic_roundtrip.rsx`
   - `examples/batch_info.rsx`
   - `examples/mosaic_debug.rsx`
10. Public docs were updated to explain the split and the public/private boundary.

## Current Development Direction

- Continue strengthening the package boundary between the private Engine and the public application layer
- Expand public-facing docs that explain system organization without exposing core internals
- Keep `roadscript-cli` reviewable through examples, tests, and tooling
- Continue shaping `roadscript-site` as the public-facing website and demo layer
