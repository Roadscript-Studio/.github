# Roadscript

Roadscript is building an authenticity tooling ecosystem around media provenance, invisible watermarking workflows, and developer-facing verification tools.

The project is organized as a public/private repository system: public repositories show the application layer, documentation, and website surface, while the core engine implementation remains private during productization.

## Public repositories

| Repository | Status | Purpose |
|---|---:|---|
| [`roadscript-docs`](https://github.com/Roadscript-Studio/roadscript-docs) | Public | Public overview, architecture notes, repository boundaries, and development milestones. |
| [`roadscript-cli`](https://github.com/Roadscript-Studio/roadscript-cli) | Public | Standalone C++ CLI, workflow DSL, local TUI prototype, examples, tests, and tooling. |
| [`roadscript-site`](https://github.com/Roadscript-Studio/roadscript-site) | Public | Public website and demo surface for Roadscript. |

## Private core

The core engine repository, `roadscript-engine`, is private. It contains the portable C++ watermarking engine and exports the internal package boundary used by the public application layer:

- CMake package: `RoadscriptEngine`
- Exported target: `Roadscript::rsengine`

The engine source and implementation internals are intentionally not public while the technology is still being developed and productized.

## Architecture boundary

Roadscript is split into clear layers:

```text
roadscript-docs
  public overview and architecture notes

roadscript-site
  public website and demo surface

roadscript-cli
  public CLI, workflow DSL, local TUI prototype, tests, and examples

roadscript-engine
  private C++ core package and implementation
