# Roadscript

Roadscript is building an authenticity tooling ecosystem for media provenance, invisible watermarking workflows, and developer-facing verification tools.

The first product family under Roadscript is **Cyphra**: an image authenticity and verification system powered by a private portable C++ core package, public developer tooling, documentation, and product-facing demo surfaces.

## Product hierarchy

```text
Roadscript
├── Cyphra
│   ├── Roadscript Engine
│   ├── Cyphra CLI
│   ├── Cyphra SDKs
│   └── Cyphra Apps
├── Roadscript Docs
└── Roadscript Site
```

Roadscript is the umbrella ecosystem. Cyphra is the product family. Roadscript Engine is the private core technology package behind Cyphra, while Cyphra CLI is the public developer-facing command-line and workflow layer.

## Public repositories

| Repository | Status | Purpose |
|---|---:|---|
| [`roadscript-docs`](https://github.com/Roadscript-Studio/roadscript-docs) | Public | Public overview, architecture notes, repository boundaries, and development milestones. |
| [`roadscript-cli`](https://github.com/Roadscript-Studio/roadscript-cli) | Public | Public repository for Cyphra CLI: the standalone C++ CLI, workflow DSL, local TUI prototype, examples, tests, and tooling. |
| [`roadscript-site`](https://github.com/Roadscript-Studio/roadscript-site) | Public | Public website and sample-driven demo surface for Roadscript and Cyphra. |

## Private core

The private core repository, `roadscript-engine`, contains **Roadscript Engine**: the portable C++ package behind Cyphra.

It provides the internal package boundary used by the public application layer:

- CMake package: `RoadscriptEngine`
- Exported target: `Roadscript::rsengine`

The Engine source and implementation internals are intentionally not public while the technology is still being developed and productized.

## Architecture boundary

Roadscript is organized into clear public and private layers:

```text
roadscript-docs
  public overview, repository map, and architecture notes

roadscript-site
  public website and sample-driven demo surface

roadscript-cli
  public Cyphra CLI repository: CLI, workflow DSL, local TUI prototype, tests, examples, and tooling

roadscript-engine
  private Roadscript Engine repository: portable C++ core package and implementation
```

The public repositories show system architecture, application-layer engineering, documentation discipline, and developer workflow design without exposing private core implementation details.

## Current status

Roadscript is under active development. Current public work focuses on:

- public/private repository boundaries
- Roadscript Engine as a private installable C++ package
- Cyphra CLI as a public developer-facing workflow layer
- public documentation and architecture notes
- website and demo presentation
- future SDK and app integration planning

The public repositories are intended for project review, portfolio review, and high-level collaboration discussion. They should not be interpreted as a finished commercial release.

## For reviewers

This organization demonstrates:

- C++ package boundary design
- CMake export/consume architecture
- CLI application design
- workflow DSL structure
- local TUI prototyping
- documentation and repository hygiene
- public/private IP boundary management
- product hierarchy planning across Engine, CLI, SDK, apps, docs, and site

Start with [`roadscript-docs`](https://github.com/Roadscript-Studio/roadscript-docs) for the full repository map and architecture overview.
