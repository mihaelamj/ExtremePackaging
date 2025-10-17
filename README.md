# ExtremePackaging

A reference architecture for building modular Swift projects using **Swift Package Manager** as the foundation.

## Overview

**ExtremePackaging** is a project template and methodology focused on **maximal modularity** and **minimal coupling**.
Each feature or domain is isolated into its own Swift package with a single, clear responsibility — making the codebase faster to build, easier to reason about, and naturally scalable across iOS, macOS, and server targets.

## Core Principles

- **Isolate everything.** Each package is self-contained with its own dependencies.
- **Share only contracts.** Communication happens through public interfaces, never implementations.
- **Scale gradually.** The architecture grows in defined stages, from a simple package setup to a complete multi-platform workspace.
- **Automate hygiene.** SwiftLint and SwiftFormat keep every stage clean and consistent.

## Project Structure

```
ExtremePackaging/
├── Apps/
│   ├── iOSApp/
│   └── macOSApp/
├── Packages/
│   ├── AppFeature/
│   └── SharedModels/
└── Main.xcworkspace
```

- **Packages** contain all shared logic (features, models, utilities).
- **Apps** act as thin platform shells.
- **Workspace** ties everything together for development.

## Getting Started

```bash
git clone https://github.com/mihaelamj/ExtremePackaging.git
cd ExtremePackaging
xed .
```

Each stage of the repo represents a checkpoint in the project’s evolution:
1. 🏁 **Stage 01** – Initialize packages
2. ⚙️ **Stage 02** – Add workspace
3. 💻 **Stage 03** – Add iOS & macOS apps

Switch between stages using Git branches to explore how modularity grows step by step.

```bash
git checkout stage/03-apps-added
```

## Tooling

Built-in support for:
- 🧹 **SwiftLint** for static analysis
- 🧾 **SwiftFormat** for consistent style
- 🧱 **SwiftPM** for dependency isolation

All configurations are included and ready to extend per package.

## Why It Matters

ExtremePackaging promotes an architecture that remains transparent as it scales.
By embracing modular design from day one, teams can iterate faster, test independently, and keep codebases healthy — even in long-lived projects.

---

> *“Design for separation, not complexity.”*

